---
layout: default
title: 文章列表
---
#{{ page.title }}
{% for post in site.posts %}
*	[{{ post.title }}]({{ site.baseurl}}{{ post.url }})
	{{ post.excerpt }}
{% endfor %}
