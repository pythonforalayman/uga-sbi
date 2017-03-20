---
layout: page
navigation_title: Resources
title: Resources
index: 5
---

We have put together a page of resources we think will be helpful to you as your continue on your journey towards proficiency in Business Intelligence. Please consider using them to your advantage.

{% for resource in site.data.resources %}
{% capture modulo %}{% cycle 'open', '0', 'close' %}{% endcapture %}
{% if modulo == 'open' %}
<div class="row" style="margin: 0px">
{% endif %}
    <div class="col-sm-12 col-md-4">
        <a href="{{ resource.url }}"><img src="{{ resource.photo }}"></a>
        {{ resource.description }}
    </div>
{% if modulo == 'close' %}
</div>
{% endif %}
{% endfor %}

<br /><br />
# Recent News

{% for news in site.data.news %}
{% capture modulo %}{% cycle 'open', 'close' %}{% endcapture %}
{% if modulo == 'open' %}
<div class="row">
{% endif %}
    <div class="col-sm-12 col-md-6 lg-top-offset">
        <a href="{{ news.url }}"><img src="{{ news.photo }}"></a>
        <span class="news-title">{{ news.title }}</span><br />
        {{ news.description }} <a href="{{ news.url }}">read more</a>
    </div>
{% if modulo == 'close' %}
</div>
{% endif %}
{% endfor %}