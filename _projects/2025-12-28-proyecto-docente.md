---
layout: default
title: "Construcción del sitio (Hub técnico y docente)"
date: 2025-12-28
nivel: "Base sólida"
promocion: "Project principal"
stack:
  - Jekyll
  - GitHub Pages
  - Markdown
  - HTML
  - CSS
---

<div class="cards-grid cards-grid--2">
  <div class="cardx">
    <div class="cardx__head">
      <div class="cardx__icon">🏗️</div>
      <div>
        <div class="cardx__title">Qué es este project</div>
        <div class="cardx__subtitle">Un hub técnico y docente</div>
      </div>
    </div>

- Centraliza **docencia + desarrollo** en un único sitio.
- Conecta **Blog** (teoría), **Projects** (práctica) y **Repositorios** (código).
- Publicación directa con **Markdown**, sin builds complejos ni dependencias pesadas.

    <div class="cardx__cta">
      <a class="btnx" href="{{ '/' | relative_url }}">Ver la web →</a>
      <a class="btnx btnx--ghost" href="{{ site.github_url | default: 'https://github.com/jpexposito/jpexposito.github.io' }}" target="_blank" rel="noopener">Repo / GitHub →</a>
    </div>
  </div>

  <div class="cardx">
    <div class="cardx__head">
      <div class="cardx__icon">🎯</div>
      <div>
        <div class="cardx__title">Objetivos</div>
        <div class="cardx__subtitle">Claridad, mantenibilidad y enlaces estables</div>
      </div>
    </div>

- Mantener una estructura simple y escalable.
- Tener un diseño coherente (botones/cards) y buena lectura en posts.
- Facilitar navegación rápida para estudiantes y desarrolladores.
  </div>
</div>

<hr/>

## Decisiones de diseño (lo importante)

> **Importante:** el sitio prioriza la lectura y la claridad por encima de “efectos”. Un hub técnico debe ser rápido, entendible y mantenible.

- **Jekyll + GitHub Pages**: hosting sencillo, gratuito y muy fácil de mantener.
- **Markdown-first**: el contenido manda; el layout acompaña.
- **CSS modular**:
  - `site.css`: layout, hero, nav, botones, estilos generales y pulido Markdown.
  - `cards.css`: sistema de cards (`cardx`), grids y componentes (chips/stack).
- **Componentes reutilizables**:
  - Cards para explicar estructura (Blog / Projects / Repos).
  - Listados (blog/projects) con look “card” para escanear rápido.

<hr/>

## Estructura del repo (resumen práctico)

- `_posts/` → entradas del blog (formato `YYYY-MM-DD-titulo.md`)
- `projects/` → índice y páginas “manuales” (ej. `projects/index.md`)
- `_projects/` → **colección** de Projects (auto-listado con `site.projects`)
- `assets/css/` → estilos (`site.css`, `cards.css`)
- `_includes/` → navegación (`nav.html`)
- `_layouts/` → `default.html` (cabecera + contenido + footer)

<hr/>

## Cómo crear un nuevo Project (plantilla rápida)

1) Crear un archivo en `_projects/` con front-matter:
```yaml
---
title: "Nombre del project"
date: 2025-12-28
nivel: "Intermedio"
promocion: "Destacado"
stack: [Jekyll, Docker, ...]
---
```

2) Escribir contenido en Markdown: problema → solución → cómo ejecutar → demo → repositorio.

3) Se lista automáticamente en `/projects/` (si tu `projects/index.md` recorre `site.projects`).

<hr/>

## Desarrollo local (opcional pero recomendado)

```bash
bundle exec jekyll serve
```

Abrir:
- `http://localhost:4000/`
- `http://localhost:4000/blog/`
- `http://localhost:4000/projects/`

<hr/>

## Mejoras futuras (ideas con impacto)

- **Projects destacados** en home (`featured: true`) y mostrar 3.
- **Buscador** simple (cliente) para blog/projects.
- Añadir **plantilla estándar de project**: problema → arquitectura → endpoints → cómo ejecutar → learnings.
- Generar automáticamente un bloque de “últimos cambios” (últimos posts + últimos projects).

<div align="center" style="margin-top: 12px;">
  <img src="{{ '/assets/images/estructura-web.png' | relative_url }}"
       width="520" style="max-width:100%; height:auto;"
       alt="Estructura del sitio">
</div>
compose -up d
```