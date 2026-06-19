---
layout: default
title: Blog
---

<section class="mimo-section">
  <div class="mimo-section__header">
    <div class="mimo-section__header-title">
      <h2>Blog</h2>
    </div>
  </div>
  {% for post in site.posts %}
  <a class="mimo-row" href="{{ post.url | relative_url }}">
    <div class="mimo-row__index"><span>{{ forloop.index | prepend: "0" | slice: -2, 2 }}</span></div>
    <div class="mimo-row__info">
      <h3>{{ post.title }}</h3>
      <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
    </div>
    <div class="mimo-row__arrow"><span>→</span></div>
  </a>
  {% endfor %}
</section>
