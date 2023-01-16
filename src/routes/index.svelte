<!-- index.svelte -->
<template>
  <div>
    <h1>Welcome to Toulouse's page</h1>
    <Video videoUrl={latestVideoUrl} />
  </div>
</template>

<script>
  import Video from '../components/Video.svelte';
  export let latestVideoUrl = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
</script>
