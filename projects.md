---
layout: page
title: projects
permalink: /projects/
---

A selection of things I'm building or have built. Source for most lives on
<a href="{% for s in site.socials %}{% if s.name == 'github' %}{{ s.url }}{% endif %}{% endfor %}">GitHub</a>.

{% for p in site.data.projects %}
<div class="entry">
  <div class="entry-title">{{ p.title }}</div>
  <div class="entry-meta">{{ p.year }}{% if p.role %} &middot; {{ p.role }}{% endif %}{% if p.stack %} &middot; {{ p.stack }}{% endif %}</div>
  <div class="entry-desc">{{ p.description }}</div>
  {% if p.links %}
  <div class="entry-links">
    {% for l in p.links %}<a href="{{ l.url }}">{{ l.label }}</a>{% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}
