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

I'm a first-year Ph.D. student at The Chinese University of Hong Kong (CUHK), supervised by Prof. <a href="https://ych133.github.io/" target="_blank" rel="noopener">Yu Cheng</a>. I received my Bachelor's degree in Information Engineering (IEEE Honor Class) from <a href="https://www.sjtu.edu.cn/" target="_blank" rel="noopener">Shanghai Jiao Tong University</a>, advised by <a href="https://faculty.sjtu.edu.cn/zhaiguangtao/en/index.htm" target="_blank" rel="noopener">Prof. Guangtao Zhai</a>. In the summer of 2024, I was fortunate to be advised by <a href="https://hszhao.github.io/" target="_blank" rel="noopener">Prof. Hengshuang Zhao</a> at HKU.

My research interests include computer vision, computer graphics, and multimodal learning.

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
- Graduated from SJTU (IEEE Honor Class in Information Engineering); awarded University Outstanding Graduate, June 2025.
- Awarded the Zhiyuan Honors Bachelor's Degree, June 2025.

# 🎖 Honors and Awards
- *2021–2023* Zhiyuan Honor Scholarship (RMB 5,000 × 4, Top 5%).
- *2024* Education Development Scholarship (RMB 5,000; rank 1/30).
- Overseas Study Scholarship (RMB 20,000).

# 📖 Education
- *2025.08 – Present*, The Chinese University of Hong Kong, Hong Kong, China.
- *2021.08 – 2025.06*, Shanghai Jiao Tong University, Shanghai, China.
- *2018.09 – 2021.06*, Jinyun High School, Zhejiang, China.

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
