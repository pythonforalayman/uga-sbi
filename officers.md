---
layout: page
navigation_title: Officers
title: Officers
index: 4
---

{% for officer in site.data.officers %}
<div class="hidden-xs hidden-sm row">
    {% capture direction %}{% cycle 'left', 'right' %}{% endcapture %}
    {% if direction == 'left' %}
        <div class="col-sm-6 col-md-4">
            <img src="{{ officer.photo }}">
        </div>
        <div class="col-sm-6 col-md-8">
            <h3>{{ officer.position }}</h3>
            <span>{{ officer.bio }}</span>
        </div>
    {% else %}
        <div class="col-sm-6 col-md-8">
            <h3>{{ officer.position }}</h3>
            <span>{{ officer.bio }}</span>
        </div>
        <div class="col-sm-6 col-md-4">
            <img src="{{ officer.photo }}">
        </div>
    {% endif %}
</div>
{% endfor %}

<div class="visible-xs visible-sm">
{% for officer in site.data.officers %}
<div class="row lg-top-offset">
    <div class="col-sm-6 col-md-4">
        <img class="small-img" src="{{ officer.photo }}">
    </div>
    <div class="col-sm-6 col-md-8">
        <h3>{{ officer.position }}</h3>
        <span>{{ officer.bio }}</span>
    </div>
</div>
{% endfor %}
</div>