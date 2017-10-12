---
layout: page
title: Maratón Linuxero en vivo
---
<div align="center">
<video id="media" width="100%" controls autoplay="true" poster="/media/poster-directo.png">
	<source src="http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.ogg" type="audio/ogg" />
	<source src="http://emision.maratonlinuxero.org/redirect.php?m=emision_audiohd.mp3" type="audio/mp3" />
</video>
  
<b><i>Calidad de transmisión</i></b>
<br />
<button id="button-hd" name="quality" onclick="reload_hd()" style="font-size:32px;"><b>HD</b></button>
<button id="button-sd" name="quality" onclick="reload_sd()" style="font-size:32px;">SD</button>

<br />
<br />

<button onclick="reload_chat()" style="font-size:24px;">Recargar chat</button>
<iframe id="chat" src="https://kiwiirc.com/client/irc.freenode.net:6667/#maratonlinuxero" style="border:0; width:100%; height:500px;"></iframe>
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
		
		document.getElementById("button-hd").innerHTML = "<b>HD</b>";
		document.getElementById("button-sd").innerHTML = "SD";
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

		document.getElementById("button-hd").innerHTML = "HD";
		document.getElementById("button-sd").innerHTML = "<b>SD</b>";
	}

	function reload_chat() {
		document.getElementById("chat").src += "";
	}
</script>
