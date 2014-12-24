---
layout: default
title: Archive
---

<ul class="posts">
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    &nbsp;
    <small class="datetime muted" data-time="{{ post.date }}">{{ post.date | date_to_string }} </small>
  </li>
  {% endfor %}
</ul>
