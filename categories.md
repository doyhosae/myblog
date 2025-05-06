---
layout: page
title: 카테고리
permalink: /categories/
---

<div class="categories-page">
  {% for category in site.categories %}
  <div class="category-section" id="{{ category[0] }}">
    <h2 class="category-title">{{ category[0] }}</h2>
    <ul class="post-list">
      {% for post in category[1] %}
        <li>
          <span class="post-date">{{ post.date | date: "%Y년 %m월 %d일" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
</div>

<style>
  .categories-page {
    margin-top: 2rem;
  }
  
  .category-section {
    margin-bottom: 3rem;
  }
  
  .category-title {
    border-bottom: 2px solid #f0f0f0;
    padding-bottom: 0.5rem;
    margin-bottom: 1rem;
  }
  
  .post-list {
    list-style: none;
    padding-left: 0;
  }
  
  .post-list li {
    margin-bottom: 0.5rem;
  }
  
  .post-date {
    color: #666;
    font-size: 0.9rem;
    margin-right: 0.5rem;
  }
</style> 