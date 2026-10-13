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

<header class="home-hero">
  <h1 class="home-hero__name">Alejandro Bandera</h1>
  <p class="home-hero__role">Profesor Ayudante Doctor · Matemática Aplicada I · Universidad de Sevilla</p>
  <p class="home-hero__summary">Mi investigación se centra en el desarrollo de técnicas de Modelado de Orden Reducido (ROM, por sus siglas en inglés) para sistemas de ecuaciones diferenciales, tanto ordinarias como en derivadas parciales. Trabajo con Proper Orthogonal Decomposition (POD), Reduced Basis (RB) y Proper Generalized Decomposition (PGD). Entre las aplicaciones destacan los sistemas dinámicos lento-rápido, los modelos de turbulencia y las EDPs elípticas.</p>
</header>

<nav class="home-actions" aria-label="Enlaces rápidos">
  <a class="home-btn" href="{{ '/cv/' | relative_url }}">CV</a>
  <a class="home-btn" href="{{ '/publications/' | relative_url }}">Publicaciones</a>
  {% if site.author.googlescholar %}<a class="home-btn" href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
  {% if site.author.orcid %}<a class="home-btn" href="{{ site.author.orcid }}">ORCID</a>{% endif %}
  {% if site.author.email %}<a class="home-btn" href="mailto:{{ site.author.email }}">Contacto</a>{% endif %}
  <a class="home-btn" href="{{ '/teaching-resources/' | relative_url }}">Recursos docentes y tutorías</a>
</nav>

<section class="home-section" id="sobre-mi">
  <h2 class="home-section__title">Trayectoria</h2>
  <div class="home-prose">
    <p>Actualmente soy Profesor Ayudante Doctor en el departamento de Matemática Aplicada I de la Universidad de Sevilla. Anteriormente he sido contratado FPI en el departamento de Ecuaciones Diferenciales y Análisis Numérico de la Universidad de Sevilla y Profesor Ayudante Doctor en el departamento de Métodos Cuantitativos de la Universidad Loyola Andalucía.</p>
    <p>Tengo un doctorado en Matemáticas, mi tesis se titula: <em>Some applications of Reduced Order Modelling to slow-fast dynamical systems, turbulence models and elliptic PDEs</em>. Soy investigador del grupo M2S2M (FQM-120) de la Universidad de Sevilla y anteriormente dentro del grupo MICA de la Universidad Loyola Andalucía.</p>
    <details class="home-more">
      <summary>Más sobre mí</summary>
      <p>He realizado estancias de investigación en Valorem/University of Bordeaux, Francia (con S. Brillet y M. Azaïez, 3 meses), y en la University of Evry, Francia (con S. Menozzi y A. Vidal, 2 meses).</p>
      <p>Me gustan los idiomas y hablo Español, Inglés, Alemán y Francés.</p>
    </details>
  </div>
</section>

<section class="home-section" id="lineas-de-investigacion">
  <h2 class="home-section__title">Líneas de investigación</h2>
  <div class="home-cards">
    <div class="home-card">
      <h3 class="home-card__title">Proper Orthogonal Decomposition (POD)</h3>
      <p>Construye una base de pocos modos óptimos a partir de simulaciones del modelo completo (<em>snapshots</em>) para reducir de forma drástica el coste de cálculo.</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Reduced Basis (RB)</h3>
      <p>Aproxima problemas parametrizados con una base construida a partir de soluciones para valores representativos de los parámetros, separando el cálculo costoso (<em>offline</em>) del rápido (<em>online</em>).</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Proper Generalized Decomposition (PGD)</h3>
      <p>Busca la solución como suma de productos de funciones de cada variable o parámetro, evitando la maldición de la dimensionalidad en problemas paramétricos.</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Aplicaciones</h3>
      <p>Sistemas dinámicos lento-rápido, modelos de turbulencia y EDPs elípticas.</p>
    </div>
  </div>
</section>

<div class="home-columns">
  <section class="home-section" id="ultimas-publicaciones">
    <h2 class="home-section__title">Últimas publicaciones</h2>
    <ul class="home-list">
      {% assign home_pubs = site.publications | sort: "date" | reverse %}
      {% for p in home_pubs limit: 3 %}
      <li>
        <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
        <span class="home-meta"><em>{{ p.venue }}</em>, {{ p.date | date: "%Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    <p class="home-viewall"><a href="{{ '/publications/' | relative_url }}">Ver todas las publicaciones &rarr;</a></p>
  </section>

  <section class="home-section" id="charlas-recientes">
    <h2 class="home-section__title">Charlas recientes</h2>
    <ul class="home-list">
      {% assign home_talks = site.talks | sort: "date" | reverse %}
      {% for t in home_talks limit: 3 %}
      <li>
        <a href="{{ t.url | relative_url }}">{{ t.title }}</a>{% if t.date > site.time %} <span class="home-badge">Próxima</span>{% endif %}
        <span class="home-meta">{{ t.venue }} &middot; {{ t.date | date: "%d/%m/%Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    <p class="home-viewall"><a href="{{ '/talks/' | relative_url }}">Ver todas las charlas &rarr;</a></p>
  </section>
</div>
