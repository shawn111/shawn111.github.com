---
layout: default
title: Slides
permalink: /presentations/
---

# Slides

分享讓我們收穫更多, 下面是我最近的一些簡報紀錄
{% for post in site.slides reversed %}
- {{ post.date | date: "%b %-d, %Y"}} [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}
