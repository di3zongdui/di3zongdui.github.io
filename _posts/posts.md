---
layout: default
title: "文章列表"
description: "郭雁冰 AI人才战略、CAIO招聘、AI转型咨询专栏文章"
permalink: /posts/
---

<section class="posts-page">
  <div class="page-header">
    <h1>专栏文章</h1>
    <p class="subtitle">AI人才战略 · CAIO招聘 · AI转型咨询</p>
  </div>

  <div class="posts-list">
    {% for post in site.posts %}
    <article class="post-item">
      <div class="post-meta">
        <span class="post-date">{{ post.date | date: "%Y年%m月%d日" }}</span>
        {% if post.categories %}
        <span class="post-category">{{ post.categories | first }}</span>
        {% endif %}
      </div>
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      {% if post.description %}
      <p class="post-excerpt">{{ post.description }}</p>
      {% elsif post.excerpt %}
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
      {% endif %}
      <a href="{{ post.url | relative_url }}" class="read-more">阅读全文 →</a>
    </article>
    {% endfor %}

    {% if site.posts.size == 0 %}
    <p class="no-posts">暂无文章，敬请期待。</p>
    {% endif %}
  </div>
</section>
