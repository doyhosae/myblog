---
layout: default
---

# 안녕하세요!

이것은 **Jekyll**과 **GitHub Pages**로 만든 첫 블로그입니다.

## 최근 게시물

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%Y-%m-%d" }}</small>
    </li>
  {% endfor %}
</ul> 