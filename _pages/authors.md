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
  <hr>
  <ul>
    {% for author in site.authors %}
      {% unless author.anonymous %}
      <br>
      <div style="margin-left: -40px">
        <figure style="float: left; margin-left: 0px; margin-right: 25px; margin-bottom: -15px; margin-top: -5px;">
          <img src="img/{{ author.image }}" style="width:128px; height:128px;">
          <figcaption style="margin-top: -10px;"><h3 class="donthyphenate"><a href="{{ author.url }}">{{ author.name }}</a></h3></figcaption>
        </figure>
        <div style="margin-top: 45px;">
        {% assign truncatedContent = '' %}
        {% assign paragraphs = author.content | split:'</p>' %}
        {% for paragraph in paragraphs limit:2 %}
          {{ truncatedContent | append: paragraph }}
          {{ truncatedContent | append: '</p>' }}
        {% endfor %}
        </div>
      </div>
      {% endunless %}
    {% endfor %}
  </ul>
{% endcapture %}

{% include sections.html %}
