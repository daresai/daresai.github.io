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
{% assign grouped_members = site.data.team_faculty | group_by: "university" %}
{% for group in grouped_members %}
<h2>{{ group.name }}</h2>
{% for member in group.items %}
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