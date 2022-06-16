---
title: Bypass Email Confirmation
date: 2022-06-16 10:54:55 +0888
categories: [Bug Bounty, Bypass]
tags: [emailbypass,bugbounty]     # TAG names should always be lowercase
---

Hello everyone. In this blog, I will share my finding How I was able to bypass the email confirmation by just paying close observation to responses. 

This is my first write up sharing so if I make mistakes let me know :)

everyone's approch is diffrent I will share my approach also in other blog so let's start how I was able to find the bypass 

I was hunting on a responsible disclosure program, let's say http://example.com/ 
when you sign-up on that website you get the confirmation of phone number first and then the email confirmation without any confirmation you are not allowed to access the website 

so first I entered my mobile number and enter the correct OTP and capture the response of that perticular request It was something like:-

![Desktop View](/assets/img/poc/Response Of OTP.png){: width="2048" height="818" }

As you can see there's the resetLink that was caught my attension and note down the response in notepad so next step is confirmation of the email so I was checking the confirmation link and I copy that link and pasted into the notepad and it was like 

``https://xyz.example.com/rp/1254545454545454545454``

Same as the Resetlink so I just copied the url and paste and recheck that if both resetlink and confirmation links are same or not and they were the same so that's how I was bypass the confirmation of the email address easy isn't it! 
I was able to bypass email confirmation without changing the response code or anything just by the observation 

TIP:- Always try to create two accounts or try to check the first correct response note it down to notepad and next time enter wrong details and check the outputs and repsponses 







