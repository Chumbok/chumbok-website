---
layout: post
title: Linux server got hacked? Todos for beginners
date: 2018-01-11T04:07:13+00:00
categories: [Tech, Hack]
tags: [Debian, Ubuntu, Linux, Hack]
author: Mossaddeque Mahmood
---
![image](/assets/images/2018-01/104168549-hack.1910x1000.jpg)

Just got email from server provided complaining about spamming from your server? CPU usages is higher than expected? Some process toke all your memory? Or OS acting weird?

Example snippets are relevant to Debian/Ubuntu, try look for command for different linux distribution.

Change password for both root and your user. Follow <a href="https://stackoverflow.com/questions/9596108/how-do-i-change-my-password-in-linux" rel="noopener" target="_blank">stackoverflow</a>.

Check what changed in /etc and /var in last 2 days:

```find /etc -mtime -2```

```find /var -mtime -2```

If you haven&#8217;t changed it, somebody did. Decide what to do with that changes.

Install ClamAV:

```sudo apt-get install clamav
sudo freshclam
sudo apt install clamav-daemon
```

Search for infected files:

```sudo clamscan --max-filesize=3999M --max-scansize=3999M --exclude-dir=/sys/* -i -r /```

Checks for signs of a <a href="https://en.wikipedia.org/wiki/Rootkit" target="_blank" rel="noopener">rootkit</a>:

Install chkrootkit:

```sudo apt-get install chkrootkit```

Run chkrootkit:

```sudo chkrootkit```

You might get some false positive, don&#8217;t panic. Google.

Security vulnerabilities comes with negligence, update your OS:

```sudo apt-get update && time sudo apt-get dist-upgrade```

Some great links that I found:  
<a href="https://security.stackexchange.com/questions/7443/how-do-you-know-your-server-has-been-compromised" target="_blank" rel="noopener">StackExchange &#8211; How do you know your server has been compromised?</a>

Cheers!