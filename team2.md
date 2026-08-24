---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---
<h1>Team</h1>
<center><img src="/images/team.jpg" style="border-radius: 0;" width="1200" height="250" align="center"></center>
<br>


{% assign universities = site.data.team_faculty | group_by: "university" %}
{% for university in universities %}
{% assign uni = site.data.universities[university.name] %}
{% assign first_member = university.items[0] %}
<div style="margin-top:50px; margin-bottom:30px;">
<a href="{{ uni.url }}"
target="_blank"
rel="noopener noreferrer"
style="text-decoration:none; color:inherit;">

<h2 style="display:flex; align-items:center;">
<img src="{{ site.url }}{{ site.baseurl }}/images/universities/{{ first_member.logo }}" alt="{{ university.name }}" style="height:60px; vertical-align:middle; margin-right:10px;"> {{ uni.name }}
</h2>
</a>
</div>

<div class="row">
{% for member in university.items %}

<div class="col-sm-4 clearfix" style="margin-bottom:25px;">
<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" style="float:left; width:30%; margin-right:8px;">
<div style="overflow:hidden;">
<h4>{{ member.name }}</h4>
{{ member.info }}<br>

{% if member.email %}
{{ member.email }}<br>
{% endif %}

{% if member.web %}
{{ member.web }}<br>
{% endif %}

{% if member.since %}
{{ member.since }}
{% endif %}
</div>

</div>

{% endfor %}

</div>

{% endfor %}