---
layout: home
title: 홈
---

# 환영합니다!

이것은 **Jekyll**과 **GitHub Pages**로 만든 블로그입니다. 마크다운으로 작성된 글을 HTML로 변환하여 정적 웹사이트를 생성합니다.

## 최근 포스트

{% for post in site.posts limit:5 %}
<div class="post-preview">
  <h2>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </h2>
  <span class="post-date">{{ post.date | date: "%Y년 %m월 %d일" }}</span>
  <p>
    {% if post.excerpt %}
      {{ post.excerpt | strip_html | truncatewords: 50 }}
    {% endif %}
  </p>
  <p>
    <a href="{{ post.url | relative_url }}">계속 읽기 &raquo;</a>
  </p>
</div>
<hr>
{% endfor %}

## 카테고리

<div class="categories">
  {% for category in site.categories %}
    <a href="{{ site.baseurl }}/categories/#{{ category[0] }}" class="category-link">
      {{ category[0] }} ({{ category[1].size }})
    </a>
  {% endfor %}
</div>

## 태그

<div class="tags">
  {% for tag in site.tags %}
    <a href="{{ site.baseurl }}/tags/#{{ tag[0] }}" class="tag-link">
      {{ tag[0] }} ({{ tag[1].size }})
    </a>
  {% endfor %}
</div>