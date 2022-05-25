---
layout: post
title: Attach debugger in IntelliJ with Spring Boot application
date: 2017-11-05T00:11:19+00:00
categories: [Programming, Tip and Tricks]
tags: [Commandline, Intellij, Debugging, Java, Spring Boot]
author: Mossaddeque Mahmood
---

![image](/assets/images/2017-11/intellij-idea_logo.png)

If you run your java application inside the IntelliJ, you can do it with the green debug button. But, if you are 
running the application from command line, like me, it's the way to go -

Step 1: Run your application with debug jvm arguments.  
```
$ mvn spring-boot:run -Drun.jvmArguments="-Xdebug -Xrunjdwp:transport=dt_socket,server=y,suspend=y,address=5005"<br />
```

Step 2: Configure IntelliJ.

  * Select menu Run -> Edit Configurations
  * Create new Remote Configuration. Default configuration works with 5005 port. Change if you see fit.
  * Connect application by running (green bug icon!) Remote Configuration created on last step.

Step 3: Happy debugging 🙂