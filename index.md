---
layout: default
title: CALDER Short Papers
---

<h1 style="margin-bottom:.375rem">CALDER Short Papers</h1>
<p style="color:var(--color-muted);margin-bottom:2rem;font-size:.9375rem">
  Accessible summaries of new research from the Center for Analysis of Longitudinal Data in Education Research.
</p>

<div class="related-list">
{% for paper in site.data.papers %}
  <div class="related-card">
    <div class="pub-type pub-type-sm">
      <svg class="pub-type-icon" height="14" width="11" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64L0 448c0 35.3 28.7 64 64 64l256 0c35.3 0 64-28.7 64-64l0-288-128 0c-17.7 0-32-14.3-32-32L224 0 64 0zM256 0l0 128 128 0L256 0zM112 256l160 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-160 0c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64l160 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-160 0c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64l160 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-160 0c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>
      Short Paper
    </div>
    <h3 class="related-card-title">
      <a href="{{ paper.url }}">{{ paper.title }}</a>
    </h3>
    <div class="related-card-authors">{{ paper.authors }}</div>
    <div class="related-card-date" style="display:flex;align-items:center;gap:.75rem;flex-wrap:wrap">
      <span>{{ paper.year }}{% if paper.paper_number %} &middot; {{ paper.paper_number }}{% endif %}</span>
      {% if paper.github_url %}
      <a href="{{ paper.github_url }}" style="font-size:.75rem;display:inline-flex;align-items:center;gap:.3em;color:var(--color-muted)">
        <svg height="12" width="12" viewBox="0 0 496 512" aria-hidden="true" style="fill:currentColor"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 389.5 8 244.8 8z"/></svg>
        GitHub
      </a>
      {% endif %}
    </div>
    {% if paper.research_areas %}
    <div class="tag-list tag-list-sm" style="margin-top:.5rem">
      {% for area in paper.research_areas %}
      <span class="tag">{{ area }}</span>
      {% endfor %}
    </div>
    {% endif %}
  </div>
{% endfor %}
</div>
