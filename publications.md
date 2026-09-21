---
title: Publications
---

# Publications

## Conference Publications

{% assign conf = site.data.publications | where: 'type', 'conference' %}
{% assign years = conf | map: 'year' | uniq | sort | reverse %}
{% for y in years %}
<div class="year-group">
  <h3>{{ y }}</h3>
  {% assign pubs = conf | where: 'year', y %}
  {% for pub in pubs %}
  <div class="pub-card{% if pub.image %} has-image{% endif %}">
    {% if pub.image %}<img class="pub-figure" src="{{ pub.image | uri_escape | relative_url }}" alt="">{% endif %}
    <div class="pub-body">
      <div class="pub-title">{{ pub.title }}</div>
      <div class="pub-meta">{{ pub.authors }}</div>
      <div class="pub-meta">{{ pub.venue }}</div>
      {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
    </div>
  </div>
  {% endfor %}
</div>
{% endfor %}

## Journal Publications

{% assign journal = site.data.publications | where: 'type', 'journal' %}
{% assign years = journal | map: 'year' | uniq | sort | reverse %}
{% for y in years %}
<div class="year-group">
  <h3>{{ y }}</h3>
  {% assign pubs = journal | where: 'year', y %}
  {% for pub in pubs %}
  <div class="pub-card{% if pub.image %} has-image{% endif %}">
    {% if pub.image %}<img class="pub-figure" src="{{ pub.image | uri_escape | relative_url }}" alt="">{% endif %}
    <div class="pub-body">
      <div class="pub-title">{{ pub.title }}</div>
      <div class="pub-meta">{{ pub.authors }}</div>
      <div class="pub-meta">{{ pub.venue }}</div>
      {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
    </div>
  </div>
  {% endfor %}
</div>
{% endfor %}
