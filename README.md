---
title: Welcome
permalink: /
layout: default
---
# Welcome
Hi, welcome to my personal website. This is the place where all my crazy ramblings, how-to's and blog posts will live.

## About me
I am Stan Overgauw, 24 years old and a Ethical Hacker/Red Teamer. I have a bachelors of ICT and currently hold the certifications for GPEN, OSCP and OSWE.

## Blog posts
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}