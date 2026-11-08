---
layout: academic
title: Publications
permalink: /publications/
description: "Publications and work in preparation by Theo Avila."
---
<div class="page-intro">
  <p class="eyebrow">Papers & ongoing work</p>
  <h1>Publications<span class="accent">.</span></h1>
  <p class="page-lead">Research on climate impacts and uncertainty.</p>
  <a href="{{ site.scholar_url }}">Google Scholar <span aria-hidden="true">↗</span></a>
</div>

<section class="publication-section" aria-labelledby="published-title">
  <div class="section-heading"><h2 id="published-title">Published</h2></div>
  {% assign published = site.data.publications | where: 'status', 'published' | sort: 'year' | reverse %}
  {% assign years = published | group_by: 'year' %}
  {% for year in years %}
  <div class="publication-year">
    <h3 class="year-heading">{{ year.name }}</h3>
    <div>{% for paper in year.items %}{% include publication.html paper=paper %}{% endfor %}</div>
  </div>
  {% endfor %}
</section>

<section class="publication-section" aria-labelledby="preparation-title">
  <div class="section-heading"><h2 id="preparation-title">In preparation</h2></div>
  {% assign drafts = site.data.publications | where: 'status', 'in-preparation' %}
  {% for paper in drafts %}{% include publication.html paper=paper %}{% endfor %}
</section>
