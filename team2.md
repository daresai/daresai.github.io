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


{% assign universities = site.data.team | group_by: "university" %}

{% for university in universities %}

<div class="university-header">
  <img
    src="{{ '/assets/images/universities/' | append: university.name | slugify | append: '.png' | relative_url }}"
    alt="{{ university.name }} logo"
    class="university-logo"
  >

  <h2>{{ university.name }}</h2>
</div>

<div class if person.photo %}
    <img src/team/' | append: person.photo | relative_url }}
    {% endif %}

    <h3>{{ person.name }}</h3>

    {% if person.info %}
    <p>{{ person.info }}</p>
    {% endif %}

    {% if person.email %}
    <p>
      mailto:{{ person.email }}">
        {{ person.email }}
      </a>
    </p>
    {% endif %}

    {% if person.web %}
    <p>
        <a hrefon.web }}Webpage
        </a>
    </p>
    {% endif %}

  </div>
  {% endfor %}
</div>

{% endfor %}

</div>

</div>

{% endfor %}

</div>

</div>

{% endfor %}