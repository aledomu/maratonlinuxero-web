---
layout: page
title: Métodos de contacto
permalink: /contacto
---

Si quieres <strong>contactar</strong> con nosotros lo puedes hacer a través de:
<ul>
 	<li>Twitter: <a href="https://twitter.com/maratonlinuxero">@maratonlinuxero</a></li>
  <li>Mastodon: <a href="https://mastodon.social/@maratonlinuxero">@maratonlinuxero</a></li>
  <li>Hashtag: <a href="https://twitter.com/hashtag/Marat%C3%B3nLinuxero">#MaratónLinuxero</a></li>
 	<li>Correo: <a href="mailto:maratonlinuxero@disroot.org">maratonlinuxero@disroot.org</a> <a href="mailto:maratonlinuxero@gmail.com">maratonlinuxero@gmail.com</a></li>
 	<li>Web: <a href="/">maratonlinuxero.github.io</a></li>
  <li>Grupo de Telegram: <a href="http://t.me/maratonlinuxero">@maratonlinuxero</a></li>
  <li>Canal de YouTube: <a href="https://www.youtube.com/maratonlinuxero">Maratón Linuxero</a></li>
  <li>Radio Oficial: <a href="http://radiomaraton.ml/">Radio Maratón</a></li>
  <li>Podcast Maratón Linuxero: <a href="/feed.xml">Feed Maratón Linuxero</a></li>
  <li>Podcast Maratón Linuxero formato ogg: <a href="/feed_ogg.rss">Feed ogg Maratón Linuxero</a></li>
  <li>Audios en Archive.org: <a href="https://archive.org/details/@maratonlinuxero">Maratón Linuxero</a></li>
</ul>

O escribiéndonos directamente en nuestro <strong>formulario de contacto:<strong>

<form id="contact-form" method="post" action="https://formspree.io/maratonlinuxero@gmail.com">

  <div class="form-group">
    <div class="form-label">
      <label for="name">Nombre:</label>
    </div>
    <div class="form-field">
      <input type="text" id="name" name="name" tabindex="1" required />
    </div>
  </div>

  <div class="form-group">
    <div class="form-label">
      <label for="email">Email:</label>
    </div>
    <div class="form-field">
      <input type="email" id="email" name="email" tabindex="2" required />
    </div>
  </div>

  <div class="form-group">
    <div class="form-label">
      <label for="message">Mensaje:</label>
    </div>
    <div class="form-field">
      <textarea id="message" name="message" tabindex="3" required></textarea>
    </div>
  </div>

  <input type="hidden" name="_next" value="{{ site.baseurl | prepend: site.url }}/mensaje-enviado" />
  <input type="text" name="_gotcha" style="display:none" />
  <input type="hidden" name="_subject" value="Mensaje del formulario de contacto" />
  <input type="hidden" name="_language" value="es" />


  <p><input type="submit" value="Enviar" tabindex="4" /></p>
</form>

<div style="text-align:center; font-weight:bold;">
  No dudes en colaborar en el Maratón Linuxero. ¡Apúntate y participa!
</div>
