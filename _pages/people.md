---
layout: page
permalink: /people/
title: People
description:
nav: true
nav_order: 7
---

{% for group in site.data.people.groups %}{% if group.members.size > 0 %}
<h3 class="people-group">{{ group.name }}</h3>
<div class="people-grid">
{% for p in group.members %}
  <div class="person">
    {% if p.image %}<img class="person-img" src="{{ p.image | prepend: '/assets/img/' | relative_url }}" alt="{{ p.name }}">{% endif %}
    <div class="person-name">{{ p.name }}</div>
    <div class="person-title">{{ p.title }}</div>
    <div class="person-links">
      {% if p.email %}<a href="mailto:{{ p.email }}" title="email"><i class="fa-solid fa-envelope"></i></a>{% endif %}
      {% if p.website %}<a href="{{ p.website }}" title="website"><i class="fa-solid fa-link"></i></a>{% endif %}
      {% if p.scholar %}<a href="{{ p.scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
      {% if p.github %}<a href="{{ p.github }}" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
      {% if p.linkedin %}<a href="{{ p.linkedin }}" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
{% endif %}{% endfor %}
