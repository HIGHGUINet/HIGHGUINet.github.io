---
title: Awards
---

# Awards

{% assign years = site.data.awards | map: 'year' | uniq | sort | reverse %}
{% for y in years %}
<div class="year-group">
  <h3>{{ y }}</h3>
  {% assign items = site.data.awards | where: 'year', y %}
  {% for a in items %}
  <div class="award-card">
    <div class="pub-title">{{ a.title }}</div>
    {% if a.date %}<div class="pub-meta">{{ a.date }}</div>{% endif %}
    {% if a.file %}<div class="pub-links"><a href="{{ a.file | uri_escape | relative_url }}">View</a></div>{% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}
