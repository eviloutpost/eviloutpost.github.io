---
layout: titled
title: "Le Opere del Male"
permalink: /works
---

<blockquote class="quote">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. </p>
</blockquote>
<div class="author">Cicerone, <cite>Lorem Ipsum</cite> </div>

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<p>
{% for work in site.works %}
  {% if work.layout == 'work' %}
    {% assign author = site.authors | where: 'nickname', work.author | first %}
      <h2><a href="{{ work.url }}">{{ work.title }}</a></h2>
      <i>Una creazione di <a href="{{ author.url }}">{{ author.name }}</a></i>
      <p>{{ work.caption | markdownify }}</p>
    <br>
  {% endif %}
{% endfor %}