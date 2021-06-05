<script>
  import Timer from './Timer.svelte';
  import HowTo from './HowTo.svelte';
  let audio;

  function timerEnds(e) {
    audio.play();
  }

</script>

<h1>Lavarsi le mani</h1>

<Timer on:end={timerEnds} />

<HowTo />

<h3>
  <a href="https://www.salute.gov.it/imgs/C_17_opuscoliPoster_193_allegato.pdf">sorgente immagine</a>
  <a href="https://freesound.org/people/metrostock99/sounds/345086/">sorgente sonora</a>
</h3>

<audio bind:this={audio} src="sound.wav" />


<style>
  h1, h3 {
    text-align: center;
  }
</style>
