---
title: "技术博客"
layout: default
permalink: /Blogs/
---


<section class="Blogs-listing">
  <h1>最新文章</h1>
  
  {% for post in site.Blogs reversed %}
    <div class="Blogs-item">
      <h2>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <div class="post-excerpt">
        {{ post.excerpt | truncate: 160 }}
      </div>
      <div class="post-meta">
        <time>{{ post.date | date: "%Y-%m-%d" }}</time> • 
        分类: {{ post.category }} • 
        阅读时间: {{ post.content | number_of_words | divided_by: 180 | plus: 1 | append: '分钟' }}
      </div>
    </div>
    <hr>
  {% endfor %}
</section>
