---
layout: page
title: Noticias
permalink: /noticias/
---
En forma de blog añadiremos las noticias que vayan surgiendo previas a la Maratón.

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <h5><div class="post-meta">{{ post.date | date: "%d/%m/%Y" }}</div></h5>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ post.url }}" class="read-more">Sigue leyendo...</a>
    </article>
  {% endfor %}
</div>
