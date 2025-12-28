---
layout: default
title: Projects
permalink: /projects/
---

<h2 class="blog__title">Mis proyectos</h2>

<ul class="blog__list">
  {% assign items = site.projects | sort: "date" | reverse %}
  {% for p in items %}
    <li class="blog__item">
      <a class="blog__link" href="{{ p.url | relative_url }}">{{ p.title }}</a>

      <div class="blog__date">
        {% if p.date %}{{ p.date | date: "%Y-%m-%d" }}{% endif %}
        {% if p.nivel %} · {{ p.nivel }}{% endif %}
        {% if p.promocion %} · {{ p.promocion }}{% endif %}
      </div>

      {% if p.stack %}
        <div class="project__stack">
          {% for t in p.stack %}
            <span class="project__pill">{{ t }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
