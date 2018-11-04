---
layout: titled
title: "Opere del Male"
permalink: /works
---

<blockquote class="quote">
  <p>I libri per tutti sono sempre libri maleodoranti: l'odore della piccola gente resta loro attaccato addosso.</p>
</blockquote>
<div class="author">Friedrich Nietzsche, <cite>Al di là del bene e del male</cite> </div>

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