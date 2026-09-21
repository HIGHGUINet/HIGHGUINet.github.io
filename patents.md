---
title: Patents
---

# Patents

{% assign items = site.data.patents | sort: 'year' | reverse %}
{% for p in items %}
<div class="pub-card">
  <div class="pub-title">{{ p.title }}</div>
  <div class="pub-meta">{{ p.country }}{% if p.number != "" %} · {{ p.number }}{% endif %} · {{ p.year }}</div>
</div>
{% endfor %}
