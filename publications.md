---
layout: page
title: publications
permalink: /publications/
---

{% assign pubs = site.data.publications | sort: "year" | reverse %}

{% for p in pubs %}
<div class="entry">
  <div class="entry-title">{{ p.title }}</div>
  <div class="entry-meta">
    {{ p.authors }} &middot; <em>{{ p.venue }}</em>{% if p.year %}, {{ p.year }}{% endif %}
  </div>
  {% if p.abstract %}<div class="entry-desc">{{ p.abstract }}</div>{% endif %}
  {% if p.links %}
  <div class="entry-links">
    {% for l in p.links %}<a href="{{ l.url }}">{{ l.label }}</a>{% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}
