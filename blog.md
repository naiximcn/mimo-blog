---
layout: default
title: Blog
permalink: /blog/
---

<section class="posts-page">
  <div class="section-header" style="padding-top: 2rem;">
    <p class="section-label">All Posts</p>
    <h1 class="section-title">Blog</h1>
    <p class="section-description">Thoughts, ideas, and explorations</p>
  </div>
  
  <div class="posts-list">
    {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="post-item">
      <div class="post-item-meta">
        <span class="post-card-category">{{ post.category | default: 'General' }}</span>
        <span><i class="far fa-calendar-alt"></i> {{ post.date | date: "%B %d, %Y" }}</span>
      </div>
      <h2 class="post-item-title">{{ post.title }}</h2>
      <p class="post-item-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </a>
    {% endfor %}
    
    {% if site.posts.size == 0 %}
    <div style="text-align: center; padding: 4rem 0; color: var(--text-muted);">
      <i class="fas fa-pen-nib" style="font-size: 3rem; margin-bottom: 1rem; display: block;"></i>
      <p>No posts yet. Create your first post in the <code>_posts</code> directory!</p>
    </div>
    {% endif %}
  </div>
</section>
