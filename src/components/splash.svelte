<script>
  let catState = 'idle';

  setInterval(() => {
    switch (catState) {
      case 'idle':
        catState = 'playing';
        break;
      case 'playing':
        catState = 'stretching';
        break;
      case 'stretching':
        catState = 'idle';
        break;
    }

    document.querySelectorAll('.8-bit-cat-animation img').forEach(img => {
      img.style.display = 'none';
    });
    document.querySelector(`.8-bit-cat-animation .${catState}`).style.display = 'block';
  }, 3000);
</script>

<style>
  .retro-tv {
    position: relative;
    width: 600px;
    height: 400px;
    background-image: url('retro-tv-background.png');
    background-size: cover;
  }

  .8-bit-cat-animation {
    position: absolute;
    bottom: 20px;
    right: 20px;
    width: 100px;
    height: 100px;
 

  }
</style>

<div class="retro-tv">
  <iframe src="https://www.youtube.com/embed/your_video_id" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  <div class="8-bit-cat-animation">
    <img src="8-bit-cat-idle.png" alt="8-bit cat idle" class="idle" />
    <img src="8-bit-cat-playing.png" alt="8-bit cat playing" class="playing" style="display: none;" />
    <img src="8-bit-cat-stretching.png" alt="8-bit cat stretching" class="stretching" style="display: none;" />
  </div>
</div>
