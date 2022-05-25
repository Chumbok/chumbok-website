---
layout: post
title: Debug HTTP calls from code using Wireshark
date: 2017-11-16T15:27:55+00:00
categories: [Programming, Tip and Tricks]
tags: [Debugging, Wireshark]
author: Mossaddeque Mahmood
---
## Wireshark Filter

Http calls from code are pretty common now a days. Sometime it is very difficult to understand when calls are failing, 
lot of things could go wrong. For example -

  1. Server firewall might be blocking the call.
  2. My firewall could be the issue.
  3. Maybe server not accepting the call because I'm not sending right param or header.

However, one of my favourite tool to debug this kind of situation [Wireshark](https://www.wireshark.org). Install it 
from [here](https://www.wireshark.org/). You can check this [video](https://youtu.be/rLfYuO6pdVA) to learn it or see 
tutorial online.

Once you have installed and running the application, you can separate network calls that you are making from your code 
using filter.

![image](/assets/images/2017-11/Wireshark_screenshot.png)

Use following filter:
`ip.dst == 10.200.96.106 && http`

_ip.dst_ is the ip of destination server and _http_is refers to calls from browser.

Happy debugging 🙂