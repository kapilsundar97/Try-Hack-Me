# [Day 6] Security Misconfiguration

- Security Misconfigurations are distinct from the other Top 10 vulnerabilities, because they occur when security could have been configured properly but was not.
- For more info, I recommend having a look at the [OWASP top 10 entry for Security Misconfiguration](https://owasp.org/www-project-top-ten/OWASP_Top_Ten_2017/Top_10-2017_A6-Security_Misconfiguration)

## Writeup
**[Task 20]**\

 **Hint: Can you find the app's source code? Maybe the documentation gives you default credentials that you can try.**
 
- After surfing through all the webpages of the web app, we can be pretty sure that the documentation is not on the box.
- So, we can go to GitHub and maybe search for **Pensive Note** over there. 
- And the first repository that pops up belongs to **NinjaJc01** who is the creator of this room as well. 
- So, all we need to do next is to read the documentation (README.md) and obtain the much-awaited default credentials. Using these credentials we can login on the web app and get the flag!
