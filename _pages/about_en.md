---
permalink: /en/
title: "About me"
lang: en
translation_url: /
author_profile: true
layout: single
classes: wide
---

<div style="text-align: justify">

<p>I am a Lecturer (Profesor Ayudante Doctor) in the Department of Applied Mathematics I at Universidad de Sevilla. Previously, I held an FPI (pre-doctoral) contract in the Department of Differential Equations and Numerical Analysis of the University of Seville (Spain), and was a Lecturer in the Department of Quantitative Methods at Universidad Loyola Andalucía. </p>

<p>My research focuses on the development of Reduced Order Modelling (ROM) techniques for systems of differential equations. My research topics also include: Proper Orthogonal Decomposition (POD), Reduced Basis (RB) and Proper Generalized Decomposition (PGD). Applications concern: Slow-fast dynamical systems, turbulence models and elliptic PDEs.</p>

<p>I have a PhD in Mathematics. I have been a researcher at the University of Seville in the research group of Profs. Tomás Chacón Rebollo and Macarena Gómez-Mármol.</p>

<p>I have been a visiting researcher at the University of Bordeaux, France (with S. Brillet and M. Azaïez, 3 months), and at the University of Evry, France (with S. Menozzi and A. Vidal, 2 months).</p>

<p>I speak Spanish, English, German and French.</p>

</div>

<nav class="home-links" aria-label="Quick links">
  <a class="btn btn--primary" href="{{ '/cv_eng/' | relative_url }}">CV</a>
  <a class="btn btn--primary" href="{{ '/teaching-resources/' | relative_url }}">Teaching resources and office hours</a>
  <a class="btn btn--primary" href="{{ '/publications/' | relative_url }}">Publications</a>
  {% if site.author.googlescholar %}<a class="btn btn--primary" href="{{ site.author.googlescholar }}">Google Scholar</a>{% endif %}
  {% if site.author.orcid %}<a class="btn btn--primary" href="{{ site.author.orcid }}">ORCID</a>{% endif %}
</nav>

<section class="home-section" id="research-lines">
  <h2 class="home-section__title">Research lines</h2>
  <ul class="home-list">
    <li><strong>Proper Orthogonal Decomposition (POD)</strong></li>
    <li><strong>Reduced Basis (RB)</strong></li>
    <li><strong>Proper Generalized Decomposition (PGD)</strong></li>
    <li><strong>Applications:</strong> slow-fast dynamical systems, turbulence models and elliptic PDEs</li>
  </ul>
</section>

<section class="home-section" id="latest-publications">
  <h2 class="home-section__title">Latest publications</h2>
  <ul class="home-list">
    {% assign home_pubs = site.publications | sort: "date" | reverse %}
    {% for p in home_pubs limit: 3 %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a><br>
      <span class="home-meta"><em>{{ p.venue }}</em>, {{ p.date | date: "%Y" }}</span>
    </li>
    {% endfor %}
  </ul>
  <p class="home-more"><a href="{{ '/publications/' | relative_url }}">View all publications &rarr;</a></p>
</section>

<section class="home-section" id="recent-talks">
  <h2 class="home-section__title">Recent talks</h2>
  <ul class="home-list">
    {% assign home_talks = site.talks | sort: "date" | reverse %}
    {% for t in home_talks limit: 3 %}
    <li>
      <a href="{{ t.url | relative_url }}">{{ t.title }}</a>{% if t.date > site.time %} <span class="home-badge">Upcoming</span>{% endif %}<br>
      <span class="home-meta">{{ t.venue }} &middot; {{ t.date | date: "%B %-d, %Y" }}</span>
    </li>
    {% endfor %}
  </ul>
  <p class="home-more"><a href="{{ '/talks/' | relative_url }}">View all talks &rarr;</a></p>
</section>
