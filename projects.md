---
layout: page
title: My Projects
permalink: /projects/
---

Here are the projects I've been working on:

{% for post in site.posts %}
  ### [{{ post.title }}]({{ post.url }})
  *{{ post.date | date: "%B %e, %Y" }}*
  {{ post.excerpt }}
{% endfor %}
