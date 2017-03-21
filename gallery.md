---
layout: page
navigation_title: Gallery
title: Gallery
index: 6
---

{% for i in (1..4) %}
<div class="row top-offset">
{% for x in (1..4) %}
{% assign url = "https://unsplash.it/400/?random" %}
<div class="col-lg-3 col-md-3 col-sm-12 sm-offset">
    <a href="{{ url }}"><img src="{{ url }}"></a>
</div>
{% endfor %}
</div>
{% endfor %}