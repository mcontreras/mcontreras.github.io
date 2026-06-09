---
title: Etiquetas
permalink: /etiquetas/
description: Archivo de notas por etiquetas y temas específicos.
layout: default
---
<div class="notes-page">
  <div class="wrap">
    <div class="page-head">
      <h1 class="page-title">Etiquetas</h1>
      <p class="page-desc">Temas concretos para moverte por el archivo con más precisión.</p>
    </div>

    {% assign tags = site.tags | sort %}
    <div class="taxonomy-index">
      {% for tag in tags %}
      {% assign tag_name = tag[0] %}
      {% assign tag_posts = tag[1] %}
      {% assign tag_slug = tag_name | slugify %}
      <section class="archive-group" id="{{ tag_slug }}">
        <div class="archive-group-head">
          <h2 class="archive-group-title">#{{ tag_name }}</h2>
          <span class="archive-group-count">{{ tag_posts | size }} notas</span>
        </div>
        {% include posts_list.html posts=tag_posts excerpt_length=120 date_format="%-d %b '%y" %}
      </section>
      {% endfor %}
    </div>
  </div>
</div>
