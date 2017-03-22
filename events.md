---
layout: page
navigation_title: Events
title: Apply to the Exec Board!
index: 2
---
<div class="row">
<div class="col-md-12 col-sm-12">
{% capture text %}
<h4>
  <b>Apps due March 30 at 5PM</b>
</h4>  
<h5 class="center bold">
  <a href="https://docs.google.com/forms/d/1lSdddbWcUiZGIiSqDwlFFIo0mJmKHs4AP-ZpgT93w5Q/edit">APPLY HERE</a>
</h5>
<span>
  Our executive board applications are officially open - if you're a freshman, sophomore, junior, or rising senior, please apply to be a part of this incredible leadership experience. We have 5 positions open - <b>VP of Marketing, VP of Finance, VP of Internal Relations, VP of External Relations, and VP of Web Development</b>. You can apply for a maximum of 2 positions, and we will review applications by April 3rd. If selected, you will be asked to interview with either our President (Alisha Jiwani) or our Vice President (Alisha Merchant). Please email us if you have any questions. The link below contains the application and more details about each position along with the key roles involved with each. Please keep in mind that the deadline is March 30. We can't wait to hear from you all!
</span>
{% endcapture %}
{% capture image %}
<img src="http://ugasbi.weebly.com/uploads/8/0/8/1/80816214/exec-1_1_orig.png">
{% endcapture %}
<div class="row">
  <div class="col-md-6 col-sm-12">
    {{ text }}
  </div>
  <div class="col-md-6 col-sm-12 sm-offset">
    {{ image }}
  </div>
</div>
</div>
</div>

<div class="row top-offset">
{% capture currentDate %}{{'now' | date: '%s' }}{% endcapture %}
<div class="clearfix">
  <h1 class="event-time-heading fix-top">Future {% if site.event_label %} {{site.event_label}} {% else %} Events {% endif %} </h1>
  {% for post in site.posts reversed %}
  {% capture blogDate %}{{post.date | date: '%s' }}{% endcapture %}
  {% if blogDate >= currentDate %}
    <a href="{{ post.url | prepend: site.baseurl }}">
      {% if post.cover %}
        <div class="event-square" style="background-image:url({{post.cover}});">
        {% else %}
          <div class="event-square" style="background-image:url(http://evento.io/img/cover.jpg);">
          {% endif %}
          <h2>{{ post.title }} <span>{{ post.date | date: "%b %-d, %Y" }} at {{ post.date | date: "%I:%M%p" }}</span></h2>
          <div class='event-square-overlay'></div>
        </div>
        
      </a>
    {% endif %}
  {% endfor %}
</div>
<div class="clearfix">
  <h1 class="event-time-heading">Past {% if site.event_label %} {{site.event_label}} {% else %} Events {% endif %} </h1>
  {% for post in site.posts %}
  {% capture blogDate %}{{post.date | date: '%s' }}{% endcapture %}
  {% if blogDate < currentDate %}
    <a href="{{ post.url | prepend: site.baseurl }}">
      {% if post.cover %}
        <div class="event-square" style="background-image:url({{post.cover}});">
        {% else %}
          <div class="event-square" style="background-image:url(http://app-beacon.com/wp-content/uploads/2015/05/events.jpg);">
          {% endif %}
          <h2>{{ post.title }} <span>{{ post.date | date: "%b %-d, %Y" }}  at {{ post.date | date: "%I:%M%p" }}</span></h2>
          <div class='event-square-overlay'></div>
        </div>
        
      </a>
    {% endif %}
  {% endfor %}
</div>
</div>