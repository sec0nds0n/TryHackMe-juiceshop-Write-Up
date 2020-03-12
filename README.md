# TryHackMe-juiceshop-Write-Up-
[WRITE-UP] TryHackMe! - Juice Shop Rooms 

Juice Shop TryHackMe

Credits to OWASP and Bjorn Kimminich


Task 1: Connect To Our Network  

    it's easy man....

Task 2: Configure Burp(If you haven't already) 

    Just follow the instruction

Task 3: Walk through the application 

     No need to answer  

Task 4: Injection

    Trying insert single quote (') on login page, and you should get SQLi vuln
    Try SQLi : admin' or 1=1--
    In main page, tap f12 and open the network
    Filter to JS, and check all the JS files
    Search sensible directory for “admin” or something else
    Got the admin page and all the users
        email : admin@juice-sh.op
        domain : juice-sh.op

Task 5: Broken Authentication


      login with SQLi:
        email : jim@juice-sh.op' and 1=1--
        password : jim@juice-sh.op' and 1=1--  
     
    open your burp, and find some sensible sign like “token” maybe?
    check the token with token decoder!
    found some password?
    crack it!
     



    for the jim's eldest siblings middle name
       1) i search “[password that you found] + jim” combination of name + password
       2) found word “star trek” and his captain is james, not jim.
       3) you've to get some social engineering skills

Task 6:

    From the hint, we should get access to see “terms of use” page. 
    trying to access “about us” to get more information 
    seems there is some link on there, because of different text color 
    see the link “/ftp” 
    its sound interesting to access! 

Task 7:

    Already done. Check Task 4!
