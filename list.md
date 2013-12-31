---
layout: default
navId: list
title: 文章列表
---
{% for post in site.posts %}
* [{{ post.title }}]({{ site.baseurl}}{{ post.url }}) --- {{ post.date | date: "%Y-%m-%d %H:%M:%S" }}
{% endfor %}
