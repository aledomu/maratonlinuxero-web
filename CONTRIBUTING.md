# Guía de contribución

En el [README](README.md) se indica cómo está compuesto el sitio web.


## Escribir posts

En el caso de los posts es además necesario que las cabeceras contengan valores para `title` (título), `date` (fecha en el que se escribió, en formato yyyy-mm-dd), `category` (Noticias o Podcast, dependiendo del tipo de post) y `tags` (etiquetas separadas por comas). Ejemplo:

	---
	layout: post
	title: "Vamos a morir todos"
	date: 666-06-06
	category: Noticias
	tags: [fin del mundo, apocalipsis]
	---

Si es la entrada correspondiente a un podcast, también hay que escribir:

	---
	(...)
	category: Podcast
	(...)
	youtube:
	  id: (lo que va después de "https://www.youtube.com/watch?v=" o "https://youtu.be/")
	podcast:
	  audio: (enlace al archivo de audio sin extensión)
	  video: (igual que arriba pero para el archivo de vídeo, si hay)
	---

Y al final de la redacción (los letreros pueden cambiarse a gusto):

	Aquí tenéis el vídeo en YouTube:
	
	{% include youtubePlayer.html %}
	
	Y aquí el audio:
	
	{% include audioPlayer.html %}
	
	Estas son nuestras vías de contacto:
	
	{% include links.html %}

Dentro del directorio `_posts` hay más ejemplos representativos.

### Pautas de redacción
* Hay que escribir en formato [GFM (Markdown, versión de GitHub)](https://github.com/ricval/Documentacion/blob/master/Guias/GitHub/mastering-markdown.md). Para escribir en una nueva línea dentro del mismo párrafo hay que acabar la línea previa con dos espacios.
* El [nombre del archivo][1] solo puede contener caracteres alfanuméricos reconocidos por el alfabeto inglés. A su vez, este debe ir precedido de la fecha en formato inverso con guiones, es decir, `YYYY-MM-DD-(nombre)`.
* Usar solo `*` en las listas no ordenadas, nada de `+` o `-`, sin líneas vacías entre elementos y con identado de 2 espacios para sublistas, es decir:

    	* elemento1
    	* elemento2
    	  * elemento2.1
    	  * elemento2.2
    	* elemento3

* No usar numeración de varios niveles en las sublistas ordenadas, es decir:

    	1.
    	  1.1.
    	  1.2.

    Esto no está permitido. En su lugar hay que escribir:

    	1.
    	  1.
    	  2.

    O en su defecto, que la sublista no sea ordenada (lo recomendado si la lista va a tener más de un subnivel).
* En las listas hay que terminar las líneas sin puntos, salvo que haya un desarrollo/descripción de cierta extensión (como en este caso).
* Todas las fechas deben ser escritas en horario español **peninsular** (UTC+1 en horario estándar), y especificarlo explícitamente tal como está aquí indicado.
* Nunca crear títulos en nivel h1, es decir, que empiecen por una única `#`.
* Las descripciones a pie de imagen deben escribirse en nivel h6, que en markdown sería `###### ` delante del texto que escribas.
* **Cuida la ortografía, las mayúsculas-minúsculas y la puntuación, así como la claridad y *universalidad* de expresión. Recuerda que somos leídos por personas de muchos países de habla hispana, cada uno con sus giros lingüísticos particulares.** Es preferible tardar un poco más en lanzar una publicación si eso supone poder escribir de forma más serena y con mayor calidad. (PD: es **YouTube**, no Youtube)
* Al escribir enlaces u otros datos del evento como el @ de Twitter, el email, etc, es **muy** recomendable llamar la variable que contiene la información (`{{ site.variable }}` o `{{ page.variable }}`) en lugar de escribir directamente el dato, tal como se indica en la siguiente sección. Si tienes dudas sobre este punto, óbvialo o consulta a @aledomu por aquí en GitLab o por su correo.
* Es preferible integrar los enlaces en el texto, tal que [así](https://maratonlinuxero.org), en lugar de <https://maratonlinuxero.org>.
* **Para los enlaces a <archive.org> hay que usar los de tipo permalink como se explica [aquí](https://archive.org/help/video.php) para que en caso de que hagan alguna migración de servidores el hipervínculo siga funcionando.** Por otra parte, su embed no funciona, así que no se puede usar.


## Para el sitio web

En caso de que quieras mantener, mejorar o aportar algo más allá de la redacción o correcciones a la web, aquí tienes unas **pautas**:
* Usa identado con **dos espacios**, no tabulador.
* Ten en cuenta que esta página va a ser mantenida *principalmente* por redactores, de los cuales no todos tienen los conocimientos suficientes para entender las plantillas y los estilos CSS, y mucho menos para JavaScript, así que si vas a implementar alguna función nueva haz que sea configurable mediante valores desde `_config.yml` o la página específica, usando `{{ site.variable }}` o `{{ page.variable }}`, respectivamente. En el primer caso, documéntalo comentando los valores que crees en el mismo `_config.yml`, y en el segundo caso documéntalo en la sección "Cómo escribir posts" de este archivo.
* Haz el código lo más legible que puedas.
* Sigue los flujos de lógica más simples y cortos. Si estás ante la duda de si elegir entre que sean entendibles o sean rápidos, elige que sea entendible.
* Si vas a modificar un archivo ya existente, presta atención a los patrones de escritura del código y síguelos.
* Y lo más importante **siempre**: *haz lo **máximo** posible con lo **mínimo** indispensable.* Usa el ingenio ;)


## Enviar contribuciones

Si no tienes permisos de edición directa del repositorio, emplea el clásico método de forkear el repositorio y hacer un Merge Request (o Pull Request, para los que están acostumbrados a GitHub) con los cambios. Además, nos viene bien que borres tu fork si tus cambios han sido aceptados para que el contador de forks nos sea representativo.

Si tienes permisos de edición directa del repositorio, haz los cambios directamente si ya han sido acordados con el resto de organizadores del evento. Si es para una sugerencia o para probar una funcionalidad nueva que quieres compartir con los demás, abre un branch nuevo en el repositorio y haz los cambios ahí. Una vez acordado, se introducirán los cambios en la rama principal.
