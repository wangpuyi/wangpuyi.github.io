---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

I'm a third year undergraduate student from School of Electronic Information and Electrical Engineering, [Shanghai Jiao Tong University](https://www.sjtu.edu.cn/). I am very fortunate to be advised by [Prof. Hengshuang Zhao](https://www.XXX.com/) from HKU. I was advised by [Prof. Guangtao Zhai](https://faculty.sjtu.edu.cn/zhaiguangtao/zh_CN/index.htm) from SJTU.

My research interest includes computer vision, computer graphics, machine learning, and computational photography.

# 📝 Publications 
{% assign pubs = site.data.publications | default: empty %}
{% if pubs and pubs.size > 0 %}
<ul class="pubs-list">
  {% for p in pubs %}
  <li style="margin-bottom:0.8rem">
    <div class="pub-title">
      {% if p.paper_url %}<a href="{{ p.paper_url }}" target="_blank" rel="noopener">{{ p.title }}</a>{% else %}{{ p.title }}{% endif %}
    </div>
    <div class="pub-authors">{{ p.authors }}</div>
    <div class="pub-venue">
      {{ p.venue }}
      {% if p.doi %} · <a href="https://doi.org/{{ p.doi }}" target="_blank" rel="noopener">DOI</a>{% endif %}
      {% if p.code_url %} · <a href="{{ p.code_url }}" target="_blank" rel="noopener">Code</a>{% endif %}
      {% if p.pdf_url %} · <a href="{{ p.pdf_url }}" target="_blank" rel="noopener">PDF</a>{% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
{% endif %}

# 🔥 News


# 🎖 Honors and Awards
- *2021&22&23* Zhiyuan Honor Scholarship (￥5000*3, Top 5%). 
- *2024* Education Development Scholarship （￥5000, rank 1/30）. 

# 📖 Educations
- *2021.08 - 2025.06*, Shanghai Jiao Tong University, Shanghai, China. 
- *2018.09 - 2021.06*, Jinyun High School, Zhejiang, China. 


# 💻 Internships
{% assign interns = site.data.internships | default: empty %}
{% if interns and interns.size > 0 %}
<ul class="internships">
  {% for i in interns %}
  <li style="margin-bottom:0.8rem">
    <div class="intern-company">
      <strong>{{ i.company }}</strong>
      {% if i.timeline %}<span style="opacity:0.8"> ({{ i.timeline }})</span>{% endif %}
    </div>
    {% if i.supervisor %}<div class="intern-supervisor">Supervisor: {{ i.supervisor }}</div>{% endif %}
    {% if i.project_name and i.project_url %}
      <div class="intern-project">Project: <a href="{{ i.project_url }}" target="_blank" rel="noopener">{{ i.project_name }}</a></div>
    {% endif %}
    {% if i.location %}<div class="intern-location" style="opacity:0.85">{{ i.location }}</div>{% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>Waiting for update.</p>
{% endif %}
