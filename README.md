# Introducción

Este es el repositorio del sitio web del Maratón Linuxero y su feed RSS, los cuales están generados con Jekyll.


# Información sobre Jekyll

Jekyll es un generador de páginas web estáticas y feeds escrito en Ruby. Para crear dichas páginas, admite texto plano escrito en varios formatos tipo markdown con inserciones en [Liquid](https://help.shopify.com/themes/liquid) y de código HTML. Para más información:
* <https://gitlab.com/pages/jekyll/blob/master/README.md>
* <https://jekyllrb.com/docs/home/>


# Licencia(s) del proyecto

El contenido de la web y el material multimedia hecho íntegramente por los participantes de este proyecto está bajo la licencia Creative Commons BY-SA, y el código de la web se encuentra bajo la licencia AGPLv3. El material multimedia que tome obras de terceros pueden tener otras licencias, siempre Creative Commons y siendo especificada.

Los podcast hasta el evento "Maratón Linuxero 3D" del 3 de diciembre de 2017, excepto el "Maratón Linuxero 1.1" del 15 de octubre de 2017, están bajo licencia Creative Commons BY-NC-SA.


# Estructura de los contenidos

Los enlaces que se encuentran en la cabecera **visible** de la página son generados a partir de los archivos *.md* de la raíz del repositorio. En el caso de los posts que se encuentran resumidos en la página principal, son los archivos dentro de la carpeta `_posts`. Es requisito indispensable que los primeros especifiquen en su cabecera `layout: page` y los segundos `layout: post`.

Para cambiar la imagen del reproductor de la radio de la página principal hay que reemplazar el archivo `PosterDirecto.png` dentro del directorio `media`.

**Los nombres de los documentos y de los archivos dentro de las carpetas `media` y `docs` solo pueden contener caracteres alfanuméricos sin tilde. No pueden tener *ñ*, espacios ni ningún símbolo que no sea "`-`".**


# Configuración del sitio web y las páginas

Los valores de ajuste del sitio web en su totalidad se encuentran en [_config.yml](_config.yml). Dichos valores son llamados desde los documentos y las plantillas mediante Liquid, siendo precedidos de `site.`. Cada página puede especificar más valores en su cabecera de la siguiente forma al principio del documento (al ser llamados, serían precedidos de `page.`):

	---
	variable1: valor1
	variable2: valor2
	variable3: valor3
	(...)
	---

## Cuenta atrás

Los valores de la cuenta atrás se encuentran en [_config.yml](_config.yml) bajo la variable padre `countdown`.


## Reproductor de la página principal

La portada del reproductor es tomada del archivo [/media/PosterDirecto.png](/media/PosterDirecto.png). Para cambiarla hay que mover la imagen a reemplazar a [/media/posters-directos-pasados](/media/posters-directos-pasados) y colocar la nueva portada en la misma localización que la anterior.


## Módulos

Existen ciertos trozos de código que se pueden introducir en la página usando la instrucción `{% include archivo.html opcion=valor %}`. `archivo.html` es el nombre del archivo correspondiente a dicho módulo, los cuales están en la carpeta `_includes`, y `opcion="valor"` es el parámetro con el que puede llamarse, lo cual depende del módulo. Pueden especificarse varias opciones, cada una separada de un espacio. Si alguno de los parámetros obligatorios no son indicados, el módulo no se activará. Para la redacción de posts, los módulos de esta página son los siguientes.

### audioPlayer.html

Inserta un reproductor de audio en el lugar del documento donde se llame a este archivo. Parámetros:

* **audio**: Opcional si el mismo valor está especificado en la cabecera del post, a no ser que se quiera reproducir un audio distinto. Indica el enlace del archivo de audio a reproducir, sin su extensión. Solo soporta archivos OGG Vorbis, MP3 y WAV, por orden de preferencia.


### videoPlayer.html

Inserta un reproductor de vídeo en el lugar del documento donde se llame a este archivo. Parámetros:

* **video**: Opcional si el mismo valor está especificado en la cabecera del post, a no ser que se quiera reproducir un vídeo distinto ya que tiene preferencia sobre éste. Indica el enlace del archivo de vídeo a reproducir, sin su extensión. Solo soporta archivos WebM, OGG Theora y MP4/H.264, por orden de preferencia.
* **width**: Opcional si el mismo valor en `_config.yml` o el valor `height` ya están especificados, a no ser que se quiera una cifra diferente ya que tiene preferencia sobre `_config.yml` y el valor calculado a partir de `height`. Indica el ancho del reproductor de vídeo en píxeles.
* **height**: Opcional si el mismo valor en `_config.yml` o el valor `height` (sea al llamar el módulo o en `_config.yml`) ya están especificados, a no ser que se quiera una cifra diferente ya que tiene preferencia sobre `_config.yml` y el valor calculado a partir de `height`. Indica el ancho del reproductor de vídeo en píxeles.


### youtubePlayer.html

Inserta un reproductor de vídeo de YouTube en el lugar del documento donde se llame a este archivo. Parámetros:

* **id**: Opcional si el mismo valor está especificado en la cabecera del post, a no ser que se quiera reproducir un vídeo distinto ya que tiene preferencia sobre éste. Indica el código identificador de vídeo de YouTube, es decir, lo que va después de `https://www.youtube.com/watch?v=` o `https://youtu.be/`.
* **h**: Opcional. Indica la hora de la duración del vídeo en la que establecer el comienzo de la reproducción. Toma preferencia sobre el valor del mismo parámetro en la cabecera del post, el cual solo aplica si no se indica un `id` o éste es igual al de la cabecera.
* **m**: Opcional. Indica el minuto de la duración del vídeo en la que establecer el comienzo de la reproducción. Toma preferencia sobre el valor del mismo parámetro en la cabecera del post, el cual solo aplica si no se indica un `id` o éste es igual al de la cabecera.
* **s**: Opcional. Indica el segundo de la duración del vídeo en la que establecer el comienzo de la reproducción. Toma preferencia sobre el valor del mismo parámetro en la cabecera del post, el cual solo aplica si no se indica un `id` o éste es igual al de la cabecera.
* **width**: Opcional si el mismo valor está especificado en `_config.yml`, a no ser que se quiera una cifra diferente ya que tiene preferencia sobre `_config.yml`. Indica el ancho del reproductor de vídeo en píxeles. Solo funciona si también se indica un valor para `height` al llamar el módulo.
* **height**: Opcional si el mismo valor está especificado en `_config.yml`, a no ser que se quiera una cifra diferente ya que tiene preferencia sobre `_config.yml`. Indica el ancho del reproductor de vídeo en píxeles. Solo funciona si también se indica un valor para `width` al llamar el módulo.


### links.html

Inserta la lista de enlaces de contacto y plataformas en las que estamos presentes. Parámetros:

* **type**: Opcional. Solo se usa para mostrar una lista gráfica de enlaces en el pie de página en lugar de una textual. Solo admite el valor "footer"


# Contribuir

En [la guía de contribución](CONTRIBUTING.md) están las instrucciones para modificar o enviar contribuciones a este repositorio, ya sean posts o la estructura de la web.
