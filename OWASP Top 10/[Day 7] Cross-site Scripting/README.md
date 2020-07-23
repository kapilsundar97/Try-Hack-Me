# [Day 7] Cross-site Scripting
It’s a type of injection which can allow an attacker to execute malicious scripts and have it execute on a victim’s machine.
   - **Stored XSS** - the most dangerous type of XSS. This is where a malicious string originates from the website’s database.\
   This often happens when a website allows user input that is not sanitised (remove the "bad parts" of a users input) when inserted into the database.
   - **Reflected XSS** - the malicious payload is part of the victims request to the website.\
   The website includes this payload in response back to the user. \
   To summarise, an attacker needs to trick a victim into clicking a URL to execute their malicious payload.
   - **DOM-Based XSS** - DOM stands for Document Object Model and is a programming interface for HTML and XML documents.\
   It represents the page so that programs can change the document structure, style and content.\
   A web page is a document and this document can be either displayed in the browser window or as the HTML source.

   - **Popup's** (<script>alert(“Hello World”)</script>) - Creates a Hello World message popup on a users browser.
   - **Writing HTML (document.write)** - Override the website's HTML to add your own (essentially defacing the entire page).
   - **XSS Keylogger** (http://www.xss-payloads.com/payloads/scripts/simplekeylogger.js.html) - You can log all keystrokes of a user, \
   capturing their password and other sensitive information they type into the webpage.
   - **Port scanning** (http://www.xss-payloads.com/payloads/scripts/portscanapi.js.html) - A mini local port scanner
   
## Writeup
**[Task 21]**

 - We can simply modify popup's payload and use it.

        <script>alert("Hello")</script>
 - In JavaScript, there is an object called **window.location.hostname**. We can script our payload like,

        <script>alert(window.location.hostname)</script>
 - We can try to insert a HTML tag to get the flag like:

        <p>para</p>
 - In JavaScript, cookies can be accessed by the object document.cookies. We can script our payload

        <script>alert(document.cookies)</script>
 - We can simply select the text"XSS Playground", right-click and go to the **Inspect Element** option.\
 We can use the JavaScript object **document.queryselector** which returns the first element within the document\
 that matches the specified selector. We can script our payload
 
        <script>document.querySelector('#thm-title').textContent = 'I am a hacker'</script>
 - Paste this script in the comment box to get the flag!
  
 
