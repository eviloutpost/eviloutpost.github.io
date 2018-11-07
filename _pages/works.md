---
layout: titled
title: "Opere del Male"
permalink: /works
---

{% capture quotation %}
  <blockquote class="quote">
    <p>I libri per tutti sono sempre libri maleodoranti: l'odore della piccola gente resta loro attaccato addosso.</p>
  </blockquote>
  <div class="author">Friedrich Nietzsche, <cite>Al di là del bene e del male</cite> </div>
{% endcapture %}

{% capture centered %}
  Il Male&trade; fluisce potente nelle opere dei suoi Araldi.

  Qui troverete i più sublimi distillati delle emozioni più nere, fonti di terribile bellezza.

  Fruitene *responsabilmente*.
{% endcapture %}

{% capture justified %}
  <style>
    div.shadowed-border {
      padding: 10px;
      border: 1px outset #b9b9ac;
      box-shadow: 6px 6px 6px #dbdad0;
    }
  </style>

  <div class="shadowed-border" style="margin-top : 42px;">
  {% for work in site.works %}
    {% if work.layout == 'work' %}
      {% assign author = site.authors | where: 'nickname', work.author | first %}
        <h2><a href="{{ work.url }}">{{ work.title }}</a></h2>
        <p style="font-size: small; text-align: right;" >Una creazione di <a class="donthyphenate" href="{{ author.url }}">{{ author.name }}</a></p>
        <p>{{ work.caption | markdownify }}</p>
      <br>
    {% endif %}
  {% endfor %}
  </div>
{% endcapture %}

{% include sections.html %}
