---
layout: default
title: Blog
---

<h2 class="blog__title">Últimas entradas</h2>

<ul class="blog__list">
  {% assign posts = site.posts | sort: "date" | reverse %}
  {% for post in posts %}
    <li class="blog__item">
      <a class="blog__link" href="{{ post.url }}">
        {{ post.title }}
      </a>
      <time class="blog__date" datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%Y-%m-%d" }}
      </time>
    </li>
  {% endfor %}
</ul>
