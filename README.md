# TryHackMe-juiceshop-Write-Up
[WRITE-UP] TryHackMe! JuiceShop Rooms JuiceShop TryHackMe
![alt text](https://i.imgur.com/JaX5W2u.png)
Credits to OWASP and Bjorn Kimminich



Task 1: Connect To Our Network  

    it's easy man....

Task 2: Configure Burp(If you haven't already) 

    Just follow the instruction

Task 3: Walk through the application 

     No need to answer  

Task 4: Injection

    1. Trying insert single quote (') on login page, and you should get SQLi vuln
    2. Try SQLi : admin' or 1=1--
    3. In main page, tap f12 and open the network
    4. Filter to JS, and check all the JS files
    5. Search sensible directory for “admin” or something else
    6. Got the admin page and all the users
        email : admin@juice-sh.op
        domain : juice-sh.op
![alt text](https://ibb.co/86s3mwW)
![alt text](https://ibb.co/0fP3CHY)
Task 5: Broken Authentication


    1. login with SQLi:
        email : jim@juice-sh.op' and 1=1--
        password : jim@juice-sh.op' and 1=1--  
     
    2. open your burp, and find some sensible sign like “token” maybe?
    3. check the token with token decoder! (online tools could be an option)
    4. found some hash password? (online tools could be an option)
    5. crack it!

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
