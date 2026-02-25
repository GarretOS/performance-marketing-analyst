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
    {% if post.author %}
    By <strong>{{ post.author }}</strong><br>
    {% endif %}
    Posted on {{ post.date | date: "%B %-d, %Y" }}
  </p>
  
  {% if post.tags.size > 0 %}
  <div class="blog-tags">
    Tags:
    {% for tag in post.tags %}
    <a href="{{ '/tags' | relative_url }}#{{ tag | slugify }}">{{ tag }}</a>{% unless forloop.last %},{% endunless %}
    {% endfor %}
  </div>
  {% endif %}
  
  {% if post.thumbnail-img %}
  <div class="post-image">
    <a href="{{ post.url | relative_url }}">
      <img src="{{ post.thumbnail-img | relative_url }}" alt="{{ post.title }}">
    </a>
  </div>
  {% endif %}
  
  <div class="post-entry">
    {{ post.excerpt }}
  </div>
  
  <a href="{{ post.url | relative_url }}" class="post-read-more">[Read More]</a>
</div>

{% endfor %}
