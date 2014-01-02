---
layout: page
navId: list
title: 文章列表
---
#{{ page.title }}
{% for post in site.posts %}
* {{ post.date | date: "%Y-%m-%d" }} --- [{{ post.title }}]({{ site.baseurl}}{{ post.url }}) 
{% endfor %}