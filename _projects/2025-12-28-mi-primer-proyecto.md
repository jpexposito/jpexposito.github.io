---
layout: default
title: "Mi primer proyecto"
date: 2025-12-28
nivel: "Intermedio"
promocion: "Destacado"
stack:
  - Spring Boot
  - Docker
  - PostgreSQL
---

<div class="cards-grid cards-grid--2">
  <div class="cardx">
    <div class="cardx__head">
      <div class="cardx__icon">🧪</div>
      <div>
        <div class="cardx__title">Mi primer proyecto</div>
        <div class="cardx__subtitle">Demo para probar publicación</div>
      </div>
    </div>

    <ul class="cardx__list">
      <li><strong>Qué resuelve:</strong> ejemplo simple de project publicado con Jekyll</li>
      <li><strong>Tecnologías:</strong> Spring Boot, Docker, PostgreSQL</li>
      <li><strong>Tipo:</strong> REST API</li>
    </ul>

    <div class="cardx__cta">
      <a class="btnx" href="{{ site.github_url | default: 'https://github.com/jpexposito' }}" target="_blank" rel="noopener">
        Repositorio →
      </a>
      <a class="btnx btnx--ghost" href="#endpoints">Ver endpoints</a>
    </div>
  </div>

  <div class="cardx">
    <div class="cardx__head">
      <div class="cardx__icon">⚙️</div>
      <div>
        <div class="cardx__title">Cómo ejecutarlo</div>
        <div class="cardx__subtitle">Local / Docker</div>
      </div>
    </div>

```bash
# ejemplo
docker compose up -d
