# [Day 5] Broken Access Control
IDOR, or Insecure Direct Object Reference, is the act of exploiting a misconfiguration in the way user input is handled, to access resources you wouldn't ordinarily be able to access.

## Writeup
Read **[Task 18]** to get some idea on Broken Access Control

**[Task 19]**

 - If you login with the username **noot** and password **test1234**, you will be on URL http://10.0.0.0/login?note=1
 - You can change the parameter value **1** to some other value. You might be able to access another users note.  
 - You can get the flag!
