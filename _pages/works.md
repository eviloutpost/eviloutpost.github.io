---
layout: titled
title: "Opere del Male"
permalink: /works
---

<blockquote class="quote">
  <p>I libri per tutti sono sempre libri maleodoranti: l'odore della piccola gente resta loro attaccato addosso.</p>
</blockquote>
<div class="author">Friedrich Nietzsche, <cite>Al di là del bene e del male</cite> </div>

I più sublimi distillati delle emozioni più nere, fonti di terribile bellezza.

Il Male&trade; fluisce potente nelle opere dei suoi Araldi.

Fruitene *responsabilmente*.

<br/>

<p>
{% for work in site.works %}
  {% if work.layout == 'work' %}
    <div class="post-line"></div>
    {% assign author = site.authors | where: 'nickname', work.author | first %}
      <h2><a href="{{ work.url }}">{{ work.title }}</a></h2>
      <p style="font-size: small; text-align: right;" >Una creazione di <a href="{{ author.url }}">{{ author.name }}</a></p>
      <p>{{ work.caption | markdownify }}</p>
    <br>
  {% endif %}
{% endfor %}