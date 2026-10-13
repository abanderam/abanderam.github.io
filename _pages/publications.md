---
layout: archive
title: "Publicaciones · Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% if site.author.googlescholar %}
<div class="pub-scholar">
  <p lang="es">También puedes encontrar mis artículos en <a href="{{ site.author.googlescholar }}" rel="noopener">mi perfil de Google Scholar</a>.</p>
  <p lang="en">You can also find my articles on <a href="{{ site.author.googlescholar }}" rel="noopener">my Google Scholar profile</a>.</p>
</div>
{% endif %}

{% assign pubs_sorted = site.publications | sort: "date" | reverse %}
{% assign pubs_by_year = pubs_sorted | group_by_exp: "p", "p.date | date: '%Y'" %}

<div class="pub-list">
{% for year in pubs_by_year %}
  <section class="pub-year">
    <h2 class="pub-year__heading">{{ year.name }}</h2>
    {% for post in year.items %}
      {% include archive-single-pub.html %}
    {% endfor %}
  </section>
{% endfor %}
</div>

<script>
(function () {
  function fallbackCopy(text) {
    var ta = document.createElement('textarea');
    ta.value = text; ta.setAttribute('readonly', '');
    ta.style.position = 'fixed'; ta.style.opacity = '0';
    document.body.appendChild(ta); ta.select();
    var ok = false;
    try { ok = document.execCommand('copy'); } catch (e) {}
    document.body.removeChild(ta);
    return ok;
  }
  document.querySelectorAll('.pub-btn--copy').forEach(function (btn) {
    var label = btn.textContent;
    btn.addEventListener('click', function () {
      var el = document.getElementById(btn.getAttribute('data-cite-target'));
      if (!el) return;
      var text = el.textContent.trim().replace(/\s+/g, ' ');
      function done(ok) {
        btn.textContent = ok ? btn.getAttribute('data-copied') : 'No se pudo copiar';
        setTimeout(function () { btn.textContent = label; }, 2000);
      }
      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(text).then(function () { done(true); }, function () { done(fallbackCopy(text)); });
      } else { done(fallbackCopy(text)); }
    });
  });
})();
</script>
