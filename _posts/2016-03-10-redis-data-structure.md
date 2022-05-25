---
layout: post
title: Redis ডাটা স্টাকচার
date: 2016-03-10
categories: [tech]
tags: [টেকনোলজি, রেডিস]
author: Maruf Hassan
---
**Redis ডাটা স্টাকচার**

রেডিসে ৫ ধরনের ডাটাস্টাকচার আছে। এই পাচঁ ধরনের ডাটা স্ট্রাকচার ঠিক মত বুঝতে পারলেই রেডিস বুঝা শেষ। 🙂

1. স্ট্রিং (String)
2. হ্যাশ (Hash)
3. লিস্ট (List)
4. সেট (Set)
5. অর্ডার সেট (Order Set)

**1. স্ট্রিং (String)**

এটা সবথেকে সহজ ডাটা স্ট্রাকচার। এখানে ডাটার নাম(key) ও ডাটা মিলে এই ডাটাস্ট্রাকচার তৈরি। সেট (**SET**) দিয়ে ডাটা রেডিসে জমা রাখে এবং
গেট(**GET**) দিয়ে ডাটা রেডিস থেকে বের করে।

ডাটা জমা রাখতে  
```
set <redis-key> <value>
```

যেমনঃ
```
    SET country:name "Bangladesh"
```
এখানে, **country:name** হল key এবং&#8221;**Bangladesh&#8221;** হল ভ্যালু বা আসল ডাটা।

ডাটা পেতে চাইলে  
```get <redis-key>```

যেমনঃ
```
    GETcountry:name
```


**2. হ্যাশ(Hashes)**

এখানে স্ট্রিং এর মতই একটা কী থাকে এবং তার বিপরীতে অনেকগুলো হ্যাশ কী-ভ্যালু রাখা যায়। ডাটা জমা রাখতে  
**hmset,** হ্যাশ ডাটা পাওয়ার জন্য **hget** এবং সমস্ত ডাটা পাওয়ার জন্য **hgetall** ব্যাবহার করা হয়ে থাকে।

**ডাটা জমা রাখতে চাইলেঃ**  
```
hmset <redis-ky> <hash key-value> `<hash key-value>` `<hash key-value>`
```

যেমনঃ
```
    HMSET user.info first_name Maruf last_name Hassan profession sw
```
এখানে user.info হল রেডিস কী, first\_name হল হ্যাশ কী এবং Maruf হল তার ভ্যালু। একই ভাবে last\_name আরেকটা কী তার ভ্যালু হচ্ছে Hassan।

**ডাটা পেতে চাইলেঃ**
```
hget <redis-key> <hash-key>
```
যেমনঃ
```
    hget user.info first_name
```

**সমস্ত ডাটা দেখতে চাইলেঃ**
```
hgetall <redis-key>
```
যেমনঃ
```
    hgetall user.info
```
এই পর্ব এখানেই শেষ।

### Related Posts

- [Redis – পর্ব ১]({% post_url 2016-02-17-what-is-redis-part-1 %})