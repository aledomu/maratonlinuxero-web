---
layout: page
title: Métodos de contacto
---
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
