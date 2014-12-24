---
layout: default
title: Home
---
{% for page in site.posts limit:3 %}

<div class="post">
  <!-- {% assign page = site.posts.first %} -->
  <a href="{{ page.url }}"><h1 class="post-title">{{ page.title }}</h1></a>
  <span class="post-date">{{ page.date | date_to_string }}</span>
  {{ page.content }}
</div>

{% endfor %}