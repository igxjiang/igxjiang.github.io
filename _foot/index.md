---
layout: default
permalink: /foot/  # 显式指定 URL（可选，不写则默认 /foot/）
---
<h1>Blogs</h1>
<ul>
  {% assign sorted_posts = site.foot | sort: 'date' | reverse %}  <!-- 修正为 site.foot -->
  {% for post in sorted_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.date | date: "%B %d, %Y" }}</p>
    </li>
  {% endfor %}
</ul>
