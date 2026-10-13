---
permalink: /en/
title: "About me"
lang: en
translation_url: /
author_profile: true
layout: single
classes: wide
---

<header class="home-hero">
  <h1 class="home-hero__name">Alejandro Bandera</h1>
  <p class="home-hero__role">Lecturer (Profesor Ayudante Doctor) · Applied Mathematics I · Universidad de Sevilla</p>
  <p class="home-hero__summary">My research focuses on the development of Reduced Order Modelling (ROM) techniques for systems of differential equations. My research topics include Proper Orthogonal Decomposition (POD), Reduced Basis (RB) and Proper Generalized Decomposition (PGD). Applications concern slow-fast dynamical systems, turbulence models and elliptic PDEs.</p>
</header>

<nav class="home-actions" aria-label="Quick links">
  <a class="home-btn" href="{{ '/cv_eng/' | relative_url }}">CV</a>
  <a class="home-btn" href="{{ '/publications/' | relative_url }}">Publications</a>
  {% if site.author.googlescholar %}<a class="home-btn" href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
  {% if site.author.orcid %}<a class="home-btn" href="{{ site.author.orcid }}">ORCID</a>{% endif %}
  {% if site.author.email %}<a class="home-btn" href="mailto:{{ site.author.email }}">Contact</a>{% endif %}
  <a class="home-btn" href="{{ '/teaching-resources/' | relative_url }}">Teaching resources and office hours</a>
</nav>

<section class="home-section" id="about">
  <h2 class="home-section__title">Background</h2>
  <div class="home-prose">
    <p>I am a Lecturer (Profesor Ayudante Doctor) in the Department of Applied Mathematics I at Universidad de Sevilla. Previously, I held an FPI (pre-doctoral) contract in the Department of Differential Equations and Numerical Analysis of the University of Seville (Spain), and was a Lecturer in the Department of Quantitative Methods at Universidad Loyola Andalucía.</p>
    <p>I have a PhD in Mathematics. I have been a researcher at the University of Seville in the research group of Profs. Tomás Chacón Rebollo and Macarena Gómez-Mármol.</p>
    <details class="home-more">
      <summary>More about me</summary>
      <p>I have been a visiting researcher at the University of Bordeaux, France (with S. Brillet and M. Azaïez, 3 months), and at the University of Evry, France (with S. Menozzi and A. Vidal, 2 months).</p>
      <p>I speak Spanish, English, German and French.</p>
    </details>
  </div>
</section>

<section class="home-section" id="research-lines">
  <h2 class="home-section__title">Research lines</h2>
  <div class="home-cards">
    <div class="home-card">
      <h3 class="home-card__title">Proper Orthogonal Decomposition (POD)</h3>
      <p>Builds a basis of a few optimal modes from simulations of the full model (snapshots), drastically reducing computational cost.</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Reduced Basis (RB)</h3>
      <p>Approximates parametrized problems with a basis built from solutions at representative parameter values, separating the costly (offline) stage from the fast (online) one.</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Proper Generalized Decomposition (PGD)</h3>
      <p>Seeks the solution as a sum of products of functions of each variable or parameter, avoiding the curse of dimensionality in parametric problems.</p>
    </div>
    <div class="home-card">
      <h3 class="home-card__title">Applications</h3>
      <p>Slow-fast dynamical systems, turbulence models and elliptic PDEs.</p>
    </div>
  </div>
</section>

<div class="home-columns">
  <section class="home-section" id="latest-publications">
    <h2 class="home-section__title">Latest publications</h2>
    <ul class="home-list">
      {% assign home_pubs = site.publications | sort: "date" | reverse %}
      {% for p in home_pubs limit: 3 %}
      <li>
        <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
        <span class="home-meta"><em>{{ p.venue }}</em>, {{ p.date | date: "%Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    <p class="home-viewall"><a href="{{ '/publications/' | relative_url }}">View all publications &rarr;</a></p>
  </section>

  <section class="home-section" id="recent-talks">
    <h2 class="home-section__title">Recent talks</h2>
    <ul class="home-list">
      {% assign home_talks = site.talks | sort: "date" | reverse %}
      {% for t in home_talks limit: 3 %}
      <li>
        <a href="{{ t.url | relative_url }}">{{ t.title }}</a>{% if t.date > site.time %} <span class="home-badge">Upcoming</span>{% endif %}
        <span class="home-meta">{{ t.venue }} &middot; {{ t.date | date: "%B %-d, %Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    <p class="home-viewall"><a href="{{ '/talks/' | relative_url }}">View all talks &rarr;</a></p>
  </section>
</div>
