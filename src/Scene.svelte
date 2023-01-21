<!-- Scene.svelte -->
<template>
  <div class="scene">
    <img class="background" src="background.png" alt="16-bit scene">
    <img class="cat" src="cat.png" alt="Cat using a cell phone" on:click={zoomIn}>
    <div class="cell-phone" style={cellPhoneStyle}>
      <Video videoUrl={videoUrl} />
    </div>
  </div>
</template>

<script>
  import Video from './Video.svelte';
  export let videoUrl;
  let zoomed = false;
  let cellPhoneStyle = { display: "none" };

  function zoomIn() {
    if (!zoomed) {
      zoomed = true;
      cellPhoneStyle = { display: "block" };
    } else {
      zoomed = false;
      cellPhoneStyle = { display: "none" };
    }
  }
</script>

<style>
  .scene {
    position: relative;
    width: 100vw;
    height: 100vh;
  }

  .background {
    width: 100%;
    height: 100%;
  }

  .cat {
    position: absolute;
    bottom: 10%;
    right: 10%;
    width: 20%;
    cursor: pointer;
  }

  .cell-phone {
    position: absolute;
    bottom: 10%;
    right: 10%;
    width: 50%;
    height: 50%;
    overflow: hidden;
    transition: all 0.5s ease-in-out;
  }

  .cell-phone .video {
    width: 100%;
    height: 100%;
  }
</style>
