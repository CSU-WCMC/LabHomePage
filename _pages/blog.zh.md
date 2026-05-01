---
layout: default
permalink: /zh/blog/
title: 博客
nav: false
nav_order: 1
lang: zh
ref: blog
---

<div class="post">
  <div class="header-bar">
    <h1>博客</h1>
    <h2>{{ site.blog_description }}</h2>
  </div>

{% assign postlist = site.posts | where: "lang", "zh" %}

  <ul class="post-list">
    {% for post in postlist %}
      <li>
        <h3><a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.description }}</p>
        <p class="post-meta">{{ post.date | date: '%Y-%m-%d' }}</p>
      </li>
    {% endfor %}
  </ul>
</div>
