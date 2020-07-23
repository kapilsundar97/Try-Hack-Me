# [Day 3] Sensitive Data Exposure
When a webapp accidentally divulges sensitive data, we refer to it as "Sensitive Data Exposure".

## Writeup
Skim yourself on **[Task 9]**, **[Task 10]** and **[Task 11]** to know basic knowledge on sensitive data exposure.

**[Task 12]**
 - Have a look at source code on login page. You can see the mentioned directory in it.
 - Move to mentioned directory given on **Q1**. You can see a file which likely to contain sensitive data.
 - Use these code to get the password hash of the admin user
 
        $ sqlite3 data.db
        sqlite3> .tables
        sqlite3> PRAGMA TABLE_INFO(users);
        sqlite3> SELECT * FROM USERS;
 - Crack the hash using [crack station](https://crackstation.net)
 - Login as the admin using cracked admin's password. You will get the flag! 
