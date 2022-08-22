---
title: Command Injection Guide 
date: 2022-08-22 10:54:55 +0888
categories: [Bug Bounty, Command Injection]
tags: [command Injection,bugbounty]     # TAG names should always be lowercase
---

<h1> What is Command Injection? </h1>

Command injection is an attack in which the goal is execution of arbitrary commands on the host operating system via a vulnerable application.


![Desktop View](/assets/img/poc/Injection.gif){: width="250" height="250" }

Attacker pass the bad data to the system shell through forms, cookies, and HTTP headers. This allows the attackers to gain control over a web site and carry out any action or process that the underlying application accommodates.

They typically use an input mechanism like HTML code, cookies or form fields to inject this command into the application.

<h3> Vulnerabilities That Can Lead to Command Injection </h3>

1. **Arbitrary Command Injection** <br/>
Arbitrary command injection happens when a user can submit a malicious command into an application that has the ability to run any command on the underlying host. This kind of attack might enable the attacker to obtain private information.

2. **Arbitrary File Uploads** <br/>
Whenever users are given the option to upload files with any file extension, command injection can happen if the files are kept in the site root.<br/>
![Desktop View](/assets/img/poc/upload.gif){: width="400" height="300" }

3. **Server-Side Template Injection(SSTI)** <br/>
An attacker can inject a malicious payload into a template using native template syntax and then the template is run server-side. This is known as server-side template injection.

4. **Insecure Serialization** <br/>
Improper deserialization can be leveraged to execute arbitrary commands. This is because the user-supplied serialised data is deserialized by the server-side code without being verified.

5. **XML external entity injection (XXE)** <br/>
If an application uses an XML parser that hasn’t been configured properly to parse user XML input, this can lead to Denial of Service (DoS) attacks, Server-Side Request Forgery (SSRF), and breaches to vulnerable data

<h3> How you can detect command injection attacks </h3>

![Desktop View](/assets/img/poc/Detect.gif){: width="450" height="260" }