---
title: "My records and thoughts"
layout: default
permalink: /blogs/
---

<h1>Blogs</h1>
<ul>
  {% assign sorted_posts = site.blogs | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
    {% if post.id != page.id %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>{{ post.date | date: "%B %d, %Y" }}</p>
      </li>
    {% endif %}
  {% endfor %}
</ul>
