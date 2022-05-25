---
layout: post
title: Manage JDKs in MacOS
date: 2017-11-05T00:11:19+00:00
categories: [Programming, Tip and Tricks]
tags: [Java, JDK, JDK9, MacOS, jenv]
author: Mossaddeque Mahmood
---

![image](/assets/images/2018-01/java.png)

Install JDK 9 in MacOS using [Homebrew](https://brew.sh/):

```
brew update
brew cask install java
```

All Java version get installed here: /Library/Java/JavaVirtualMachines lets take a look.  
ls -la /Library/Java/JavaVirtualMachinesList installed JDKs in your OSX:

```
$/usr/libexec/java_home -V
```

You should get result like this:
```
Matching Java Virtual Machines (5):
 9.0.1, x86_64: "Java SE 9.0.1" /Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home
 1.8.0_121, x86_64: "Java SE 8" /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home
 1.7.0_80, x86_64: "Java SE 7" /Library/Java/JavaVirtualMachines/jdk1.7.0_80.jdk/Contents/Home
 1.6.0_65-b14-468, x86_64: "Java SE 6" /Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
 1.6.0_65-b14-468, i386: "Java SE 6" /Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home/Library/Java/JavaVirtualMachines/jdk-9.0.1.jdk/Contents/Home</pre>
```
Install jenv: ```brew install jenv```

Set JDK by following `jenv` commands: http://www.jenv.be/

**Note:**_Tested on macOS Sierra._