---
layout: default
navId: home
---
#{{ page.title }}
{% for post in site.posts %}
#####[{{ post.title }}]({{ site.baseurl}}{{ post.url }})
{{ post.excerpt | strip_html }}
--------------------------------
{% endfor %}