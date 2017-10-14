---
layout: page
title: Información
---

Si quieres escuchar el directo en tu reproductor favorito, las URL son:
* Calidad HD:
  * OGG Vorbis: <{{ site.stream-base-url }}audio-hd.ogg>
  * MP3: <{{ site.stream-base-url }}audio-hd.mp3>
* Calidad SD:
  * OGG Vorbis: <{{ site.stream-base-url }}audio-sd.ogg>
  * MP3: <{{ site.stream-base-url }}audio-sd.mp3>

Para acceder al chat desde una aplicación externa, usa cualquier cliente IRC e introduce los siguientes datos:
* Servidor: **irc.freenode.net**
* Puerto: **6667**
* Canal: **#maratonlinuxero**

## Contacto

Si quieres **contactar** con nosotros lo puedes hacer a través de:

{% include links.html %}

O escribiéndonos directamente en nuestro **formulario de contacto**:

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
<br />

<img src="{{ site.avatar }}" width="200" style="float: right; margin: 5%;" />

## Acerca de nosotros

El **Maratón Linuxero** es un proyecto creado por podcasters y oyentes de GNU/Linux que quieren realizar un evento en directo a través de aplicaciones y servicios de software libre. El domingo 3 de septiembre de 15:00 a 24:00 horas (horario español peninsular, UTC+2) ofreceremos 9 horas de emisiones con podcasters de habla hispana.

**Su origen** fue ver si era posible sacar adelante emisiones en directo como otras organizaciones han hecho, pero sin recurrir a sistemas privativos, o por lo menos que sean afines al Software Libre o de código abierto.

En un principio barajamos servicios como Mumble o Butt y actualmente estamos utilizando Jitsi junto con OBS Studio para emitir en directo en YouTube, donde la facilidad de llegar a un gran número de usuarios junto con el feedback que ofrece su chat nos hizo decantarnos por esta fórmula. Realizamos pruebas que están tanto en YouTube como en formato podcast de audio. Vamos a hacer un total de 5 antes del evento del 3 de septiembre.

{% include youtubePlayer.html id="videoseries?list=PLz7ZCufmrnKJCLvFetPvz2mdiBy4vSmKf" %}

Otro aspecto que queremos resaltar es la **colaboración de empresas linuxeras españolas**. Tanto [PCUbuntu](https://www.pcubuntu.es), [VANT](http://www.vantpc.es) como [SLIMBOOK](https://slimbook.es/) no dudaron en respaldar este proyecto y sumarse a él [ofreciendo productos GNU/Linux para sorteos](/Sorteos) que realizaremos el mismo día y en la última prueba de emisiones (27 de agosto desde las 15:00 horas, UTC+2).

**La parrilla de directos** propuesta es la siguiente:

![#CartelDirectos](/media/carteldirectosmaratonlinuxero.png)
###### Obra realizada por Dan Bernal Tapia (CC BY-NC-SA)

Cada hora será conducida por uno o más divulgadores y/o podcasters de habla hispana ampliamente conocidos en comunidades GNU/Linux.

**No solo están colaborado podcasters**, sino también **administradores de sistemas, desarrolladores, diseñadores y artistas** para realizar el blog, servicios, [carteles, promos y vídeos](/Carteles-Promos-y-videos) del proyecto.

Actualmente el **[grupo de Telegram](https://telegram.me/{{ site.telegram.group }})** nos sirve para vertebrar y tomar decisiones y es una fuente de conocimientos y experiencias de esta comunidad que hemos creado en torno al Maratón Linuxero.