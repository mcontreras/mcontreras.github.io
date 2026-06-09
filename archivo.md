---
title: Archivo
permalink: /archivo/
description: Archivo cronológico de las notas publicadas.
layout: default
---
<div class="notes-page">
  <div class="wrap">
    <div class="page-head">
      <h1 class="page-title">Archivo</h1>
      <p class="page-desc">Todas las notas agrupadas por año.</p>
    </div>

    {% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
    {% for year in posts_by_year %}
    <section class="archive-group">
      <div class="archive-group-head">
        <h2 class="archive-group-title">{{ year.name }}</h2>
        <span class="archive-group-count">{{ year.items | size }} notas</span>
      </div>
      {% include posts_list.html posts=year.items excerpt_length=120 date_format="%-d %b" %}
    </section>
    {% endfor %}
  </div>
</div>
