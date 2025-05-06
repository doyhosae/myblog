---
layout: page
title: 태그
permalink: /tags/
---

<div class="tags-page">
  <div class="tags-cloud">
    {% for tag in site.tags %}
      <a href="#{{ tag[0] }}" class="tag-link" style="font-size: {{ tag[1].size | times: 5 | plus: 100 }}%;">
        {{ tag[0] }} ({{ tag[1].size }})
      </a>
    {% endfor %}
  </div>

  <hr>

  {% for tag in site.tags %}
  <div class="tag-section" id="{{ tag[0] }}">
    <h2 class="tag-title">{{ tag[0] }}</h2>
    <ul class="post-list">
      {% for post in tag[1] %}
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
  .tags-page {
    margin-top: 2rem;
  }
  
  .tags-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-bottom: 2rem;
  }
  
  .tag-link {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    background-color: #f5f5f5;
    border-radius: 20px;
    text-decoration: none;
    color: #333;
  }
  
  .tag-link:hover {
    background-color: #e0e0e0;
  }
  
  .tag-section {
    margin-bottom: 3rem;
  }
  
  .tag-title {
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