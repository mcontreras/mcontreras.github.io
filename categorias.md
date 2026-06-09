---
title: Categorías
permalink: /categorias/
description: Archivo temático de las notas por categoría.
layout: default
---
<div class="notes-page">
  <div class="wrap">
    <div class="page-head">
      <h1 class="page-title">Categorías</h1>
      <p class="page-desc">Explora las notas agrupadas por tema principal.</p>
    </div>

    {% assign categories = site.categories | sort %}
    <div class="taxonomy-index">
      {% for category in categories %}
      {% assign category_name = category[0] %}
      {% assign category_posts = category[1] %}
      {% assign category_slug = category_name | slugify %}
      <section class="archive-group" id="{{ category_slug }}">
        <div class="archive-group-head">
          <h2 class="archive-group-title">{{ category_name }}</h2>
          <span class="archive-group-count">{{ category_posts | size }} notas</span>
        </div>
        {% include posts_list.html posts=category_posts excerpt_length=120 date_format="%-d %b '%y" %}
      </section>
      {% endfor %}
    </div>
  </div>
</div>
