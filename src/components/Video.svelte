<!-- Video.svelte -->

<script>
export let videoUrl;
</script>


<template>
  <div class="video-container">
    <iframe
        title="Most recent video toulouse wants to share"
        class="video"
        src={videoUrl}
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
    ></iframe>
  </div>
</template>


<style>
  .video-container {
    position: relative;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    height: 0;
    overflow: hidden;
  }

  .video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
</style>
