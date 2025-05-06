---
layout: home
title: 홈
---

# 안녕하세요!
이것은 **Jekyll** + **GitHub Pages** 로 만든 첫 블로그입니다.

## 최근 포스트

{% for post in site.posts %}
  <article class="post-preview">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%Y년 %m월 %d일" }}
      </time>
      {% if post.categories.size > 0 %}
        <span class="categories">
          카테고리: {{ post.categories | join: ", " }}
        </span>
      {% endif %}
    </div>
    <div class="post-excerpt">
      {{ post.excerpt | strip_html | truncatewords: 50 }}
    </div>
    <a href="{{ post.url | relative_url }}" class="read-more">더 읽기 →</a>
  </article>
  <hr>
{% endfor %}