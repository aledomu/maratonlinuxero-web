---
layout: page
title: Maratón Linuxero en vivo
---
<div align="center">
<video id="media" width="100%" controls autoplay="true" poster="/media/poster-directo.png">
	<source src="http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.ogg" type="audio/ogg" />
	<source src="http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.mp3" type="audio/mp3" />
No HTML 5 support
</video>

<br />

Calidad de transmisión:
<input type="radio" name="quality" value="hd" checked onclick="reload_hd()" />HD
<input type="radio" name="quality" value="sd" onclick="reload_sd()" />SD

<br />
<br />

<input value="Recargar chat" type="button" onclick="reload_chat();">
<iframe id="chat" src="http://kiwiirc.com/client/irc.freenet.net:6667/#maratonlinuxero" style="border:0; width:100%; height:500px;"></iframe>
</div>

<script>
	function reload_hd() {
		switch(media.currentSrc) {
			case "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiosd.ogg":
				document.getElementById("media").src = "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.ogg";
				break;

			case "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiosd.mp3":
				document.getElementById("media").src = "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.mp3";
				break;
		}
	}

	function reload_sd() {
		switch(media.currentSrc) {
			case "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.ogg":
				document.getElementById("media").src = "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiosd.ogg";
				break;

			case "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.mp3":
				document.getElementById("media").src = "http://emision.maratonlinuxero.org/redirect.php?m=emision_audiosd.mp3";
				break;

		}
	}

	function reload_chat() {
		document.getElementById("chat").src += "";
	}
</script>
