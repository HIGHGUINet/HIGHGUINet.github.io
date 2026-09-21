---
title: Publications
---

# Publications

## Journal Publications

{% assign journal = site.data.publications | where: 'type', 'journal' %}
{% assign years = journal | map: 'year' | uniq | sort | reverse %}
{% for y in years %}
<div class="year-group">
  <h3>{{ y }}</h3>
  {% assign pubs = journal | where: 'year', y %}
  {% for pub in pubs %}
  <div class="pub-card">
    <div class="pub-title">{{ pub.title }}</div>
    <div class="pub-meta">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.venue }}</div>
    {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

## Conference Publications

{% assign conf = site.data.publications | where: 'type', 'conference' %}
{% assign years = conf | map: 'year' | uniq | sort | reverse %}
{% for y in years %}
<div class="year-group">
  <h3>{{ y }}</h3>
  {% assign pubs = conf | where: 'year', y %}
  {% for pub in pubs %}
  <div class="pub-card">
    <div class="pub-title">{{ pub.title }}</div>
    <div class="pub-meta">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.venue }}</div>
    {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}
