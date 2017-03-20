---
layout: page
navigation_title: Officers
title: Officers
index: 4
---

<!-- <table class="officers">
{% for officer in site.data.officers %}
<tr>
    {% capture direction %}{% cycle 'left', 'right' %}{% endcapture %}
    {% if direction == 'left' %}
        <td class="image">
            <div class="officer-square {{ direction }}">
                <img src="{{ officer.photo }}" style="width:250px">
                <h3>{{ officer.position }}</h3>
                <span>{{ officer.bio }}</span>
            </div>
        </td>
    {% else %}
        <td class="image">
            <div class="officer-square {{ direction }}">
                <h3>{{ officer.position }}</h3>
                <span>{{ officer.bio }}</span>
                <img src="{{ officer.photo }}" style="width:250px">
            </div>
        </td>
    {% endif %}
    <div class="clearfix"></div>
    </tr>
{% endfor %}
</table>
 -->

{% for officer in site.data.officers %}
<div class="row">
    {% capture direction %}{% cycle 'left', 'right' %}{% endcapture %}
    {% if direction == 'left' %}
        <div class="col-md-4">
            <img src="{{ officer.photo }}" style="width:250px">
        </div>
        <div class="col-md-8">
            <h3>{{ officer.position }}</h3>
            <span>{{ officer.bio }}</span>
        </div>
    {% else %}
        <div class="col-md-8">
            <h3>{{ officer.position }}</h3>
            <span>{{ officer.bio }}</span>
        </div>
        <div class="col-md-4">
            <img src="{{ officer.photo }}" style="width:250px">
        </div>
    {% endif %}
</div>
{% endfor %}