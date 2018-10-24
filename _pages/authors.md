---
layout: titled
title: "Esercito del Male"
permalink: /authors/
---

<blockquote class="quote">
  <p>Non c'è scusa all'essere cattivi, ma v'è un certo merito nel sapersi tali; fare il male per stupidità è il più irrimediabile dei vizi.</p>
</blockquote>
<div class="author">Charles Baudelaire, <cite>La moneta falsa</cite> </div>

<ul>
  {% for author in site.authors %}
    <li>
      <h2><a href="{{ author.url }}">{{ author.name }}</a></h2>
      <h3>{{ author.position }}</h3>
      <p>{{ author.content | markdownify }}</p>
    </li>
    <br>
  {% endfor %}
</ul>