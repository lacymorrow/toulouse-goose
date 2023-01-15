<script>
  import { fade, fly } from 'svelte/transition';

  let catImage = "https://cdn.pixabay.com/photo/2016/03/28/12/35/cat-1285634_960_720.png";
  let sunglassesImage = "https://cdn.pixabay.com/photo/2016/03/28/12/35/cat-1285634_960_720.png";
  let hollywoodImage = "https://cdn.pixabay.com/photo/2016/03/28/12/35/cat-1285634_960_720.png";
</script>

<div class="cat-container">
  <img 
    class="cat-image" 
    src={catImage} 
    transition:fade 
    alt="A 1970s cat lounging in Hollywood" 
  />
  <img 
    class="sunglasses-image" 
    src={sunglassesImage} 
    transition:fly={{ y: -50 }} 
    alt="A pair of sunglasses on the cat" 
  />
  <img 
    class="hollywood-image" 
    src={hollywoodImage} 
    transition:fade 
    alt="A view of Hollywood Hills" 
  />
</div>

<style>
  .cat-container {
    position: relative;
  }

  .cat-image {
    width: 300px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .sunglasses-image {
    width: 50px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }

  .hollywood-image {
    width: 100%;
    position: absolute;
    left: 0;
    top: 0;
  }
</style>
