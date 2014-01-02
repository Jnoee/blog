---
layout: page
navId: list
title: 文章列表
---
<h1 style="margin-top: 0px">{{ page.title }}</h1>
{% for post in site.posts %}
* {{ post.date | date: "%Y-%m-%d" }} --- [{{ post.title }}]({{ site.baseurl}}{{ post.url }}) 
{% endfor %}