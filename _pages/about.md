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

I'm a second-year Ph.D. student at The Chinese University of Hong Kong (CUHK), co-supervised by Prof. <a href="https://ych133.github.io/" target="_blank" rel="noopener">Yu Cheng</a> and Prof. <a href="https://www.cse.cuhk.edu.hk/~qdou/" target="_blank" rel="noopener">Qi Dou</a>. I received my Bachelor's degree in Information Engineering (IEEE Honor Class) from <a href="https://www.sjtu.edu.cn/" target="_blank" rel="noopener">Shanghai Jiao Tong University</a>, advised by <a href="https://faculty.sjtu.edu.cn/zhaiguangtao/en/index.htm" target="_blank" rel="noopener">Prof. Guangtao Zhai</a>. In the summer of 2024, I was fortunate to work as an intern, advised by <a href="https://hszhao.github.io/" target="_blank" rel="noopener">Prof. Hengshuang Zhao</a> at HKU.

<p style="font-size:1.1em; font-weight:600; line-height:1.6;">My research interests include code world model and coding agents for 3D worlds. Welcome for potential collaboration and internship.</p>

# 📝 Research
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
      {% assign pub_separator = "" %}
      {% if p.venue or p.status %}{{ p.venue | default: p.status }}{% assign pub_separator = " · " %}{% endif %}
      {% if p.project_url %}{{ pub_separator }}<a href="{{ p.project_url }}" target="_blank" rel="noopener">Project</a>{% assign pub_separator = " · " %}{% endif %}
      {% if p.code_url %}{{ pub_separator }}<a href="{{ p.code_url }}" target="_blank" rel="noopener">Code</a>{% assign pub_separator = " · " %}{% endif %}
      {% if p.arxiv_url %}{{ pub_separator }}<a href="{{ p.arxiv_url }}" target="_blank" rel="noopener">arXiv</a>{% assign pub_separator = " · " %}{% endif %}
      {% if p.pdf_url %}{{ pub_separator }}<a href="{{ p.pdf_url }}" target="_blank" rel="noopener">PDF</a>{% endif %}
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
- *2021–2024* Zhiyuan Honor Scholarship (RMB 5,000 × 4, Top 5%).
- *2024* Education Development Scholarship (RMB 5,000; rank 1/30).
- Overseas Study Scholarship (RMB 20,000).

# 📖 Education
- *2025.08 – Present*, The Chinese University of Hong Kong, Hong Kong, China.
- *2021.08 – 2025.06*, *rank 1/30*, Shanghai Jiao Tong University, Shanghai, China.
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
    {% if i.supervisor %}
      <div class="intern-supervisor">
        Supervisor: 
        {% if i.supervisor_url %}
          <a href="{{ i.supervisor_url }}" target="_blank" rel="noopener">{{ i.supervisor }}</a>
        {% else %}
          {{ i.supervisor }}
        {% endif %}
      </div>
    {% endif %}
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
