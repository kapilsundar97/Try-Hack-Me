# [Day 1] Injection

 - **SQL Injection**: This occurs when user controlled input is passed to SQL queries. As a result, an attacker can pass in SQL queries to manipulate the outcome of such queries. 
 - **Command Injection**: This occurs when user input is passed to system commands. As a result, an attacker is able to execute arbitrary system commands on application servers.
 
To complete the questions below, navigate to (http://MACHINE_IP/evilshell.php)

## Writeup
Skim yourself on **[Task 4]** and **[Task 5]** to know about Injection.

**[TASK 6]**
- Just give '**ls**' command in the text field to show all the files.\
 You can see a strange file in it.
- By using '**ps -ef**' command, you can lists all the users. Have a look at how many non-root/non-service/non-daemon users are there.
- Try '**whoami**'
- Use '**grep "www-data" /etc/passwd**' to see what user's shell set as.
- To know the Ubuntu's version which is running, try '**lsb_release -a**'
- As per the hint given, have a look 00-header.
