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

    <div class="explore-grid">
      <a href="{{ '/archivo/' | relative_url }}" class="explore-card">
        <span class="explore-kicker">Cronología</span>
        <strong>Archivo anual</strong>
        <span>Recorre todas las notas por año y fecha de publicación.</span>
      </a>
      <a href="{{ '/categorias/' | relative_url }}" class="explore-card">
        <span class="explore-kicker">Temas</span>
        <strong>Categorías</strong>
        <span>Encuentra artículos agrupados por enfoque editorial.</span>
      </a>
      <a href="{{ '/etiquetas/' | relative_url }}" class="explore-card">
        <span class="explore-kicker">Detalle</span>
        <strong>Etiquetas</strong>
        <span>Navega por asuntos concretos y nombres propios.</span>
      </a>
    </div>

    {% include posts_list.html posts=site.posts excerpt_length=160 date_format="%-d %b '%y" %}
  </div>
</div>
