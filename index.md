---
layout: home
navId: home
---
{% for post in site.posts %}
#####[{{ post.title }}]({{ site.baseurl}}{{ post.url }})
{{ post.excerpt | strip_html }}
--------------------------------
{% endfor %}