---
layout: default
navId: list
title: 文章列表
---
{% for post in site.posts %}
* [{{ post.title }}]({{ site.baseurl}}{{ post.url }})
{% endfor %}
