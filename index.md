---
layout: home
navId: home
---
{% for post in paginator.posts %}
###[{{ post.title }}]({{ post.url }})
{{ post.date | date: "%Y-%m-%d" }}

{{ post.summary }}

[浏览全文]({{ post.url }})
* * *
{% endfor %}
{% if paginator.total_pages > 1 %}
<ul class="pagination">
	{% if paginator.page == 1 %}
		<li class="disabled"><span>&laquo;</span></li>
	{% else %}
		<li><a href="{{ site.baseurl }}">&laquo;</a></li>		
	{% endif %}
	{% for page in (1..paginator.total_pages) %}
		{% if page == paginator.page %}
			<li class="active"><span>{{ page }} <span class="sr-only">(current)</span></span></li>
		{% else %}
			<li><a href="{{ site.baseurl }}{%if page > 1 %}/page{{ page }}/{% endif %}">{{ page }}</a></li>
		{% endif %}
	{% endfor %}
	{% if paginator.page == paginator.total_pages %}
		<li class="disabled"><span>&laquo;</span></li>
	{% else %}
		<li><a href="{{ site.baseurl }}{%if paginator.total_pages > 1 %}/page{{ paginator.total_pages }}/{% endif %}">&raquo;</a></li>
	{% endif %}
</ul>
{% endif %}