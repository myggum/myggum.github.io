---
layout: default
title: Tags
---

<ul class="tags">
{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}
  {% for data_tag in site.data.tags %}
    {% if data_tag.name == t %}
      {% assign tagname = data_tag %}
    {% endif %}
  {% endfor %}
  <li><a href="/tags/{{ tagname.slug }}">{{t | downcase | replace:" ","-" }}</a> has {{ posts | size }} posts</li>
{% endfor %}
</ul>