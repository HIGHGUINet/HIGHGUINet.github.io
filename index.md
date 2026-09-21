---
title: Home
---

<div class="profile">
  <img src="{{ '/figures/나.png' | relative_url }}" alt="Guisik Kim">
  <div>
    <h1>Guisik Kim</h1>
    <p class="tagline">Senior Researcher, Multi-Modal Research Center<br>Korea Electronics Technology Institute (KETI), Seongnam, Korea</p>
  </div>
</div>

Ph.D., School of Computer Science and Engineering, Chung-Ang University (Advisor: Prof. Junseok Kwon).
연구 관심 분야는 image dehazing, deepfake detection, low-level vision, satellite image deep learning, adverse weather scene understanding입니다.

Contact: [{{ site.email }}](mailto:{{ site.email }})

## News

{% assign recent_news = site.data.news | slice: 0, 6 %}
<ul>
{% for n in recent_news %}
  <li>[{{ n.date }}] {{ n.text }}</li>
{% endfor %}
</ul>

## Recent Publications

{% assign recent = site.data.publications | sort: 'year' | reverse | slice: 0, 3 %}
{% for pub in recent %}
<div class="pub-card">
  <div class="pub-title">{{ pub.title }}</div>
  <div class="pub-meta">{{ pub.authors }} · {{ pub.venue }}</div>
  {% if pub.pdf %}<div class="pub-links"><a href="{{ pub.pdf | uri_escape | relative_url }}">PDF</a></div>{% endif %}
</div>
{% endfor %}

<p><a href="{{ '/publications.html' | relative_url }}">전체 논문 목록 보기 →</a></p>

## Reviewer Activity

**Journals**: IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI), IEEE Transactions on Image Processing (TIP), IEEE Signal Processing Letters, Artificial Intelligence Review, Neurocomputing, Journal of Visual Communication and Image Representation (JVCIR), IEEE Geoscience and Remote Sensing Letters (GRSL)

**Conferences**: CVPR, ICCV, ECCV, BMVC, AAAI, ACCV, and NTIRE / AIM / AIMS workshops (ACCV 2022 Outstanding Reviewer Award)
