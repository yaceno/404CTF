# Reconnaissance

This web challenge allows us to see a first page that takes us to the first part of the challenge named "Authentification"
![1-1](1.png) 
![1-1](2.png) 

# Exploitation

As usual the first thing to do is checking to source code, and we found the credentials we need !

![1-1](3.png) 

Next, the second part called "Cookies".

![1-1](4.png)

It's pretty obvious that we have to modify some cookies.. Let's use BurpSuite with the intercept mode ! And bam we found a vulnerable header that we can set to true (two times)

![1-1](5.png)

Finally, the last part called "Redirect".

![1-1](5-5.png)

Using Burp with the intercept mode and reloading the page we see that it redirects to the final page containing the flag !

![1-1](6.png)
