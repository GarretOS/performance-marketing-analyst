---
layout: page
title: Projects
subtitle: My portfolio of data analytics and marketing projects
---

{% for post in site.posts %}
<div class="post-preview">
  <a href="{{ post.url | relative_url }}">
    <h2 class="post-title">{{ post.title }}</h2>
    {% if post.subtitle %}
    <h3 class="post-subtitle">{{ post.subtitle }}</h3>
    {% endif %}
  </a>
  <p class="post-meta">
    Posted on {{ post.date | date: "%B %-d, %Y" }}
  </p>
  <div class="post-entry">
    {{ post.excerpt }}
  </div>
  <a href="{{ post.url | relative_url }}" class="post-read-more">[Read More]</a>
</div>
{% endfor %}
