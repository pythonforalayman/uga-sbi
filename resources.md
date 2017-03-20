---
layout: page
navigation_title: Resources
index: 5
---

We have put together a page of resources we think will be helpful to you as your continue on your journey towards proficiency in Business Intelligence. Please consider using them to your advantage.

<table class="resources">
{% tablerow for resource in site.data.resources cols:3 %}
<a href="{{ resource.url }}"><img src="{{ resource.photo }}"></a>
{{ resource.description }}
{% endtablerow %}
</table>

<br /><br />
# Recent News
<table class="news">
{% tablerow for news in site.data.news cols:2 %}
<a href="{{ news.url }}"><img src="{{ news.photo }}"></a>
<h1>{{ news.title }}</h1>
{{ news.description }} <a href="{{ news.url }}">read more</a>
{% endtablerow %}
</table>
