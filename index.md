---
layout: default
title: 首页
---
#{{ page.title }}
{% for post in site.posts %}
*	[{{ post.title }}]({{ site.baseurl}}{{ post.url }})
	{{ post.excerpt }}
{% endfor %}