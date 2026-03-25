---
layout: default
title: Notas
permalink: /notas/
description: Artículos sobre tecnología, medios y lo que me apetezca.
---
<div class="notes-page">
  <div class="wrap">
    <div class="page-head">
      <h1 class="page-title">Notas</h1>
      <p class="page-desc">Artículos sobre tecnología, medios y lo que me apetezca.</p>
    </div>
    <div class="posts">
      {% for post in site.posts %}
      <div class="post-row">
        <span class="post-date">{{ post.date | date: "%-d %b '%y" }}</span>
        <div class="post-body">
          {% if post.categories.size > 0 %}
          <div class="post-cat">{{ post.categories | first }}</div>
          {% endif %}
          <a href="{{ post.url | relative_url }}" class="post-title">{{ post.title }}</a>
          {% if post.excerpt %}
          <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</div>
