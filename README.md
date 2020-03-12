# TryHackMe-juiceshop-Write-Up
[WRITE-UP] [TryHackMe!](https://tryhackme.com/room/juiceshop) JuiceShop Rooms JuiceShop TryHackMe
![alt text](https://i.imgur.com/JaX5W2u.png)
Credits to OWASP and Bjorn Kimminich
This machine uses the OWASP Juice Shop vulnerable web application to learn how to identify and exploit common web application vulnerabilities. This room has been designed for beginners, but can be completed by anyone.



Task 1: Connect To Our Network  

    it's easy man....

Task 2: Configure Burp(If you haven't already) 

    Just follow the instruction

Task 3: Walk through the application 

     No need to answer  

Task 4: Injection

1. Trying insert single quote (') on login page, and you should get SQLi vuln
![alt text](https://i.ibb.co/kQBnGTR/Screen-Shot-2020-03-12-at-17-15-34.png)
2. Try SQLi : admin' or 1=1--
![alt text](https://i.ibb.co/9qRjbQy/Screen-Shot-2020-03-12-at-17-19-57.png)
3. In main page, tap f12 and open the network
4. Filter to JS, and check all the JS files
![alt text](https://i.ibb.co/YtSvjYD/Screen-Shot-2020-03-12-at-17-17-33.jpg)
5. Open it! and search sensible directory for “admin” or something else
![alt text](https://i.ibb.co/9py6cwz/Screen-Shot-2020-03-12-at-17-18-14.png)
6. Got the admin page and all the users email



Task 5: Broken Authentication

1. login with SQLi:
    jim@juice-sh.op' and 1=1--
![alt text](https://i.ibb.co/2KLr6fP/Screen-Shot-2020-03-12-at-17-26-47.png)
2. open your burp, and find some sensible sign like “token” maybe?
![alt text](https://i.ibb.co/x8gxrd8/Screen-Shot-2020-03-12-at-17-26-02.jpg)
3. check the token with token decoder! (online tools could be an option)
4. found some hash password? (online tools could be an option)
5. crack it!

for the jim's eldest siblings middle name
   1) i search “[password that you found] + jim” combination of name + password
   2) found word “star trek” and his captain is james, not jim.
   3) you've to get some social engineering skills (see the question for reset jim's password)

Task 6:

1. From the hint, we should get access to see “terms of use” page.
2. trying to access “about us” to get more information 
3. seems there is some link on there, because of different text color 
![alt text](https://i.ibb.co/tZSKQZn/Screen-Shot-2020-03-12-at-17-50-17.jpg)
4. see the link “/ftp” 
5. its sound interesting to access! go on! 
![alt text](https://i.ibb.co/ZzHzGY7/Screen-Shot-2020-03-12-at-17-51-17.png)

Task 7:

    Already done. Check Task 4!
