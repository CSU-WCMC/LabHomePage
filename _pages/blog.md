---
layout: default
permalink: /en/blog/
title: blog
nav: false
nav_order: 1
lang: en
ref: blog
---

<div class="post">
  <div class="header-bar">
    <h1>{{ site.blog_name }}</h1>
    <h2>{{ site.blog_description }}</h2>
  </div>

  {% assign postlist = site.posts | where: "lang", "en" %}
  <ul class="post-list">
    {% for post in postlist %}
      <li>
        <h3><a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.description }}</p>
        <p class="post-meta">{{ post.date | date: '%B %d, %Y' }}</p>
      </li>
    {% endfor %}
  </ul>
</div>
