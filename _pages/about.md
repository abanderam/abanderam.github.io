---
permalink: /
title: "Sobre mí"
lang: es
translation_url: /en/
author_profile: true
layout: single
classes: wide
redirect_from: 
  - /about/
  - /about.html
---

<div style="text-align: justify">

<p> Actualmente soy Profesor Ayudante Doctor en el departamento de Matemática Aplicada I de la Universidad de Sevilla. Anteriormente he sido contratado FPI en el departamento de Ecuaciones Diferenciales y Análisis Numérico de la Universidad de Sevilla y Profesor Ayudante Doctor en el departamento de Métodos Cuantitativos de la Universidad Loyola Andalucía. </p>

<p> Mi investigación se centra en el desarrollo de técnicas de Modelado de Orden Reducido (ROM, por sus siglas en inglés) para sistemas de ecuaciones diferenciales, tanto ordinarias como ecuaciones en derivadas parciales. Mis campos de investigación incluyen: Proper Orthogonal Decomposition (POD), Reduced Basis (RB) y Proper Generalized Decomposition (PGD). En el ámbito de las aplicaciones destacan: los sistemas dinámicos lento-rápido, los modelos de turbulencia y EDPs elípticas. </p>

<p> Tengo un doctorado en Matemáticas, mi tesis se titula: <em>Some applications of Reduced Order Modelling to slow-fast dynamical systems, turbulence models and elliptic PDEs</em>. Soy investigador del grupo M2S2M (FQM-120) de la Universidad de Sevilla y anteriormente dentro del grupo MICA de la Universidad Loyola Andalucía. </p>

<p> He realizado estancias de investigación en Valorem/University of Bordeaux, Francia (con S. Brillet y M. Azaïez, 3 meses), y en la University of Evry, Francia (con S. Menozzi y A. Vidal, 2 meses).</p>

<p> Me gustan los idiomas y hablo Español, Inglés, Alemán y Francés. </p>

</div>

<nav class="home-links" aria-label="Enlaces rápidos">
  <a class="btn btn--primary" href="{{ '/cv/' | relative_url }}">CV</a>
  <a class="btn btn--primary" href="{{ '/teaching-resources/' | relative_url }}">Recursos docentes y tutorías</a>
  <a class="btn btn--primary" href="{{ '/publications/' | relative_url }}">Publicaciones</a>
  {% if site.author.googlescholar %}<a class="btn btn--primary" href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
  {% if site.author.orcid %}<a class="btn btn--primary" href="{{ site.author.orcid }}">ORCID</a>{% endif %}
</nav>

<section class="home-section" id="lineas-de-investigacion">
  <h2 class="home-section__title">Líneas de investigación</h2>
  <ul class="home-list">
    <li><strong>Proper Orthogonal Decomposition (POD)</strong></li>
    <li><strong>Reduced Basis (RB)</strong></li>
    <li><strong>Proper Generalized Decomposition (PGD)</strong></li>
    <li><strong>Aplicaciones:</strong> sistemas dinámicos lento-rápido, modelos de turbulencia y EDPs elípticas</li>
  </ul>
</section>

<section class="home-section" id="ultimas-publicaciones">
  <h2 class="home-section__title">Últimas publicaciones</h2>
  <ul class="home-list">
    {% assign home_pubs = site.publications | sort: "date" | reverse %}
    {% for p in home_pubs limit: 3 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a><br>
      <span class="home-meta"><em>{{ p.venue }}</em>, {{ p.date | date: "%Y" }}</span>
    </li>
    {% endfor %}
  </ul>
  <p class="home-more"><a href="{{ '/publications/' | relative_url }}">Ver todas las publicaciones &rarr;</a></p>
</section>

<section class="home-section" id="charlas-recientes">
  <h2 class="home-section__title">Charlas recientes</h2>
  <ul class="home-list">
    {% assign home_talks = site.talks | sort: "date" | reverse %}
    {% for t in home_talks limit: 3 %}
    <li>
      <a href="{{ t.url | relative_url }}">{{ t.title }}</a>{% if t.date > site.time %} <span class="home-badge">Próxima</span>{% endif %}<br>
      <span class="home-meta">{{ t.venue }} &middot; {{ t.date | date: "%d/%m/%Y" }}</span>
    </li>
    {% endfor %}
  </ul>
  <p class="home-more"><a href="{{ '/talks/' | relative_url }}">Ver todas las charlas &rarr;</a></p>
</section>
