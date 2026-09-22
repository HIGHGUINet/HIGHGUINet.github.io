---
title: Home
---

<div class="profile">
  <img src="{{ '/figures/me.png' | relative_url }}" alt="Guisik Kim">
  <div>
    <h1>Guisik Kim</h1>
    <p class="tagline">Senior Researcher, Multi-Modal Research Center<br>Korea Electronics Technology Institute (KETI), Seongnam, Korea</p>
  </div>
</div>

Ph.D., School of Computer Science and Engineering, Chung-Ang University (Advisor: Prof. Junseok Kwon).

Research interests: dehazing, deepfake detection, low-level vision, satellite image processing, and invisible watermarking.

Contact: [{{ site.email }}](mailto:{{ site.email }})

## News

{% assign recent_news = site.data.news | slice: 0, 6 %}
<ul>
{% for n in recent_news %}
  <li>[{{ n.date }}] {{ n.text }}</li>
{% endfor %}
</ul>

## Selected Publications

{% assign selected_titles = "Perturbation-Invariant Feature Based Robust Invisible Watermarking|R2M: Real-Aware Residual Model Merging for Robust and Generalizable Deepfake Detection|Siamese DINO Adapter Learning with Haze-Robust Feature Representation for Nighttime Image Dehazing" | split: "|" %}
{% for t in selected_titles %}
{% assign pub = site.data.publications | where: 'title', t | first %}
<div class="pub-card{% if pub.image %} has-image{% endif %}">
  {% if pub.image %}<img class="pub-figure" src="{{ pub.image | uri_escape | relative_url }}" alt="">{% endif %}
  <div class="pub-body">
    <div class="pub-title">{{ pub.title }}</div>
    <div class="pub-meta">{{ pub.authors }} · {{ pub.venue }}{% if pub.if %} · IF {{ pub.if }}{% endif %}</div>
    {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
  </div>
</div>
{% endfor %}

<p><a href="{{ '/publications.html' | relative_url }}">See all publications →</a></p>

## Reviewer Activity

**Journals**: IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI), IEEE Transactions on Image Processing (TIP), IEEE Signal Processing Letters, Artificial Intelligence Review, Neurocomputing, Journal of Visual Communication and Image Representation (JVCIR), IEEE Geoscience and Remote Sensing Letters (GRSL)

**Conferences**: CVPR, ICCV, ECCV, BMVC, AAAI, ACCV, and NTIRE / AIM / AIMS workshops (ACCV 2022 Outstanding Reviewer Award)
