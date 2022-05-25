---
layout: page
title: About Us
permalink: /about/
---

We are a team of software engineers who envision a digitalized world. People say, software development is 
expensive, but it doesn’t have to be and we figured out how.

Follow us in the social media: [Facebook](https://www.facebook.com/ChumbokIT) and [Twitter](https://twitter.com/ChumbokIT)

We ❤️ &nbsp; to give back to the community. Check out our projects on Github.\
Open Source Contribution: [Github](https://github.com/Chumbok)

<div>
    <h2>Founding members:</h2>
    <ul class="list">
        {% for member in site.data.members %}
        <li class="list-item">
            <div class="list-content">
                <img alt="{{ member.name }}"  src="{{ member.image }}">
                <div>
                    <b class="">{{ member.name }}</b>
                    <div>{{ member.title }}</div>
                </div>
            </div>
        </li>
        {% endfor %}
    </ul>
</div>
