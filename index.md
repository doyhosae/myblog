---
layout: default
title: 홈
---

# {{ site.title }}에 오신 것을 환영합니다!

이곳은 저의 새 블로그입니다. 앞으로 다양한 내용을 기록할 예정입니다.

## 최근 게시물
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%Y년 %m월 %d일" }}
    </li>
  {% endfor %}
</ul>