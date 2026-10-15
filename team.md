---
title: "Team"
layout: gridlay
excerpt: "Team"
sitemap: false
permalink: /team/
---
<h1>Team</h1>
<img src="{{ '/images/team.jpg' | relative_url }}" alt="DARES research team" class="img-fluid">

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
<img src="{{ '/images/universities/' | append: uni.logo | relative_url }}" alt="{{ university.name }}" style="height:60px; width:auto; vertical-align:middle; margin-right:10px;"> {{ uni.name }}
</h2>
</a>
</div>



<div class="row">

{% for member in university.items %}

<div class="col-sm-4 clearfix" style="margin-bottom:25px">
<img src="{{ '/images/teampic/' | append: member.photo | relative_url }}" alt="{{ member.name }}" class="img-fluid" style="float:left; width:30%; margin:0 12px 8px 0; border-radius: 10%">
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