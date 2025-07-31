---
title: "My records and thoughts"
layout: default
permalink: /blogs/
---

<h1>Blogs</h1>
<ul>
  {% for post in site.blogs %}
    {% if post.id != page.id %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>{{ post.date | date: "%B %d, %Y" }}</p>
      </li>
    {% endif %}
  {% endfor %}
</ul>
