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

{% assign universities = site.data.team_faculty | map: "university" | uniq %}
{% for university in universities %}
{% assign members = site.data.team_faculty | where: "university", university %}
{% assign first_member = members.first %}
<div class="university-section" style="margin-bottom:60px;">
<div style="text-align:center; margin-bottom:30px;">
<img src="{{ site.baseurl }}/images/universities/{{ first_member.logo }}"alt="{{2>

</div>
<div class="row">
{% for member in members %}
<div class="col-sm-4 clearfix" style="margin-bottom:25px;">
<img src="{{ site.url }}{{ site.baseurl }}/images/to }}"
class="img-responsive"
style="float:left; width:30%; margin-right:8px;" />
<div style="overflow:hidden;">
<h4>{{ member.name }}</h4>
<h5><i>{{ member.info }}</i></h5>
{{ member.email }}
<br>{{ member.web }}
<br>{{ member.since }}

</div>

</div>

{% endfor %}

</div>

</div>

{% endfor %}