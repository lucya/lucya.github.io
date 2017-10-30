---
title: archive
bg: tag.jpg
layout: page
permalink: "/posts/"
crawlertitle: archive
summary: Posts about jekyll
active: archive
---

{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

  <h2 class="category-key" id="{{ t | downcase }}">{{ t | capitalize }}</h2>

<!--
  <ul class="year">
    {% for post in posts %}
      {% if post.tags contains t %}
        <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span class="date">{{post.summary}}</span>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
-->
{% endfor %}