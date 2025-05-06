---
layout: home
title: 환영합니다
---

# 안녕하세요! 👋

이것은 **Jekyll**과 **GitHub Pages**로 만든 첫 블로그입니다.

## 블로그 소개

이 블로그에서는 다음과 같은 주제들을 다룹니다:

- 💻 개발 이야기
- 🍽️ 맛집 탐방
- 📚 독서 리뷰
- ✈️ 여행 기록

## 최근 게시물

{% for post in site.posts limit:3 %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>{{ post.date | date: "%Y-%m-%d" }}</small>
{% endfor %}

## 연락처

질문이나 제안이 있으시면 언제든지 [이메일](mailto:{{ site.author.email }})로 연락주세요!

또는 아래 소셜 미디어에서도 만나실 수 있습니다:
- [GitHub](https://github.com/{{ site.social.github }})
- [Twitter](https://twitter.com/{{ site.social.twitter }})
- [Instagram](https://instagram.com/{{ site.social.instagram }})

---

<div style="text-align: center; margin-top: 30px; color: #777;">
  <p>© {{ site.time | date: '%Y' }} {{ site.author.name }}. All rights reserved.</p>
</div>