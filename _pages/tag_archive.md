---
title: "Tags"
permalink: /tags/
layout: tags
author_profile: true
---

{% for tag in site.tags %}
{% for tag in work.tags %}
  <h2>{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
{% endfor %}