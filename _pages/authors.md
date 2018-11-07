---
layout: titled
title: "Esercito del Male"
permalink: /authors/
---

{% capture quotation %}
  <blockquote class="quote">
    <p>Non c'è scusa all'essere cattivi, ma v'è un certo merito nel sapersi tali; fare il male per stupidità è il più irrimediabile dei vizi.</p>
  </blockquote>
  <div class="author">Charles Baudelaire, <cite>La moneta falsa</cite> </div>
{% endcapture %}

{% capture centered %}
  Inebriati, corrotti, assetati.

  Fetidi schiavi delle nostre pulsioni, irrimediabilmente sedotti dal vacuo, dal marcio, dall'empio.

  Accecati dal nostro tossico amore per Il Male&trade;, del quale ci facciamo orgogliosamente Araldi.

  Siamo come voi, ma più *sinceri*.
{% endcapture %}

{% capture justified %}
  <ul>
    {% for author in site.authors %}
      {% unless author.anonymous %}
      <br>
      <img src="img/{{ author.image }}" style="float: left; width:128px; height:128px; margin-right:16px; margin-top:32px; margin-bottom:8px;">
      <h3 class="donthyphenate" style="display: flex;"><a href="{{ author.url }}">{{ author.name }}</a></h3>
      <h4 class="donthyphenate" style="text-align: left;">{{ author.position }}</h4>
      {% assign truncatedContent = '' %}
      {% assign paragraphs = author.content | split:'</p>' %}
      {% for paragraph in paragraphs limit:1 %}
        {{ truncatedContent | append: paragraph }}
        {{ truncatedContent | append: '</p>' }}
      {% endfor %}
      {% endunless %}
    {% endfor %}
  </ul>
{% endcapture %}

{% include sections.html %}
