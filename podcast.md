---
layout: page
title: Podcast del Maratón Linuxero
permalink: /podcast/
---

¿Te perdiste un directo? ¡No pasa nada!  
Recogeremos todos los momentos y los pondremos a disposición de la comunidad en forma de podcast.
El feed está creado desde GitLab: 
Feed mp3:<https://maratonlinuxero.org/feed.xml>  
Feed ogg:<https://maratonlinuxero.org/feed_ogg.rss>



  <div class="posts">
  {% for post in site.categories.Podcast %}
    <article class="post">

      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <h5><div class="post-meta">{{ post.date | date: "%d/%m/%Y" }}</div></h5>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ post.url }}" class="read-more">Sigue leyendo...</a>
    </article>
  {% endfor %}
</div>
