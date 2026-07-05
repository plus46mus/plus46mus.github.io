# plus46mus.github.io

<figure>
  <figcaption>Felt</figcaption>
  <audio controls src="/felt.mp3"></audio>
  <a href="felt.mp3"> Download audio </a>
</figure>

// Source - https://stackoverflow.com/a/40279892
// Posted by Justinas
// Retrieved 2026-07-05, License - CC BY-SA 3.0

$(document).ready(function() {

  $('#selection').on('change', function() {
    change($(this).val());
  });

});


function change(sourceUrl) {
  var audio = document.getElementById("player");
  var source = document.getElementById("mp3_src");

  audio.pause();

  if (sourceUrl) {
    source.src = sourceUrl;
    audio.load();
    audio.play();
  }
}

<!--
Source - https://stackoverflow.com/a/40279892
Posted by Justinas
Retrieved 2026-07-05, License - CC BY-SA 3.0
-->

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

<label for="selection">Listen:</label>
<select id="selection">
  <option value="">- Select track -</option>
  <option value="felt.mp3">felt</option>
  <option value="http://www.culturedub.com/assets/04-Moringa-JahYu-Remix-feat-BaNdula-1.mp3">Chilling on beach</option>
</select>
<br/>

<audio id="player" controls="controls">
  <source id="mp3_src" src="/teachings/2011_01_09_Cut.mp3" type="audio/mp3" />Your browser does not support the audio element.
</audio>
