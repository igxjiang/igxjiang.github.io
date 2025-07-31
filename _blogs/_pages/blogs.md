---
title: "Blogs"
layout: default
permalink: /blogs/
---

<h1>Blogs</h1>
<ul>
  {% for post in site.blogs %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.date | date: "%B %d, %Y" }}</p>
    </li>
  {% endfor %}
</ul>
