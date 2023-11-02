---
layout: page
title: ""
permalink: /gallery/
---

<style>
  .gallery-title {
    font-size: 36px;
    margin-bottom: 20px;
    color: #fff;
  }

  .gallery-table {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
    margin-top: 20px;
  }

  .gallery-image {
    width: 100%;
    border-radius: 10px;
  }

  .gallery-caption {
    font-size: 14px;
    margin-top: 10px;
    color: #ccc;
  }

  .tab-container {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
  }

  .tab {
    padding: 10px 20px;
    background-color: #333;
    color: #fff;
    border: 1px solid #444;
    border-radius: 5px;
    cursor: pointer;
    margin-right: 10px;
  }

  .tab.active {
    background-color: #555;
  }

  .gallery-container {
    display: none;
    margin-top: 20px;
  }

  .gallery-container.active {
    display: block;
  }

  @media (max-width: 768px) {
  .tab {
    margin-right: 5px;
    padding: 5px 10px;
    flex-wrap: wrap; 
  }
}
</style>

<div class="tab-container">
  <div class="tab active" onclick="showGallery('seasonal')">Tanning Season</div>
  <div class="tab" onclick="showGallery('spooky')">Spook Season</div>
  <div class="tab" onclick="showGallery('rabbit')">Rabbit Gallery</div>
  <div class="tab" onclick="showGallery('photography')">Photography Gallery</div>
</div>

<div class="gallery-container active" id="seasonal-gallery">
  <h1 class="gallery-title">Summer 2023</h1>
  <div class="gallery-table">
    <div>
      <img src="../assets/images/summer1.jpeg" alt="summer1" class="gallery-image">
      <p class="gallery-caption">Cast us for your next horror movie</p>
    </div>
    <div>
      <img src="../assets/images/summer2.jpg" alt="summer2" class="gallery-image">
      <p class="gallery-caption">I'm something of a celebrity myself</p>
    </div>
    <div>
      <img src="../assets/images/summer3.jpg" alt="summer3" class="gallery-image">
      <p class="gallery-caption">POV: You're getting buried alive</p>
    </div>
    <div>
      <img src="../assets/images/summer4.jpg" alt="summer4" class="gallery-image">
      <p class="gallery-caption">Pinkies up!</p>
    </div>
    <div>
      <img src="../assets/images/summer5.jpg" alt="summer5" class="gallery-image">
      <p class="gallery-caption">I'm actually 100ft in the air</p>
    </div>
    <div>
      <img src="../assets/images/summer6.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">Creatures of the night</p>
    </div>
    <div>
      <img src="../assets/images/summer7.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">Bro is scared of the water</p>
    </div>
        <div>
      <img src="../assets/images/summer8.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">When I paint on the walls they call it vandalism</p>
    </div>
    <div>
      <img src="../assets/images/summer9.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">The ugly duckling that stayed ugly</p>
    </div>
    <div>
      <img src="../assets/images/summer10.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">Cloud.</p>
    </div>
    <div>
      <img src="../assets/images/summer11.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">Foie Gras is discarsting</p>
    </div>
    <div>
      <img src="../assets/images/summer12.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">POV: you can't afford roads</p>
    </div>
    
  </div>
</div>

<div class="gallery-container" id="rabbit-gallery">
  <h1 class="gallery-title">Rabbit Gallery</h1>
  <div class="gallery-table">
    <div>
      <img src="../assets/images/pudding1.png" alt="Pudding 1" class="gallery-image">
      <p class="gallery-caption">She smells but not sees</p>
    </div>
    <div>
      <img src="../assets/images/pudding2.png" alt="Pudding 2" class="gallery-image">
      <p class="gallery-caption">Tranformed into bread loaf</p>
    </div>
    <div>
      <img src="../assets/images/pudding3.png" alt="Pudding 3" class="gallery-image">
      <p class="gallery-caption">Pudding dreaming about bananas</p>
    </div>
    <div>
      <img src="../assets/images/pudding4.png" alt="Pudding 4" class="gallery-image">
      <p class="gallery-caption">She has woken from her slumber</p>
    </div>
    <div>
      <img src="../assets/images/pudding5.png" alt="Pudding 5" class="gallery-image">
      <p class="gallery-caption">Pudding picking the worst spot to lounge</p>
    </div>
    <div>
      <img src="../assets/images/pudding6.png" alt="Pudding 6" class="gallery-image">
      <p class="gallery-caption">Pudding stretching before the big game</p>
    </div>
  </div>
</div>

<div class="gallery-container" id="photography-gallery">
  <h1 class="gallery-title">Photography Gallery</h1>
  <div class="gallery-table">
  </div>
</div>

<div class="gallery-container" id="spooky-gallery">
  <h1 class="gallery-title">Spooky Gallery</h1>
  <div class="gallery-table">
    <div>
      <img src="../assets/images/spook1.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Pumpkins</p>
    </div>
    <div>
      <img src="../assets/images/spook2.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">More Pumpkins</p>
    </div>
        <div>
      <img src="../assets/images/spook3.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Even More Pumpkins</p>
    </div>
        <div>
      <img src="../assets/images/spook4.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Even Even More Pumpkins</p>
    </div>
        <div>
      <img src="../assets/images/spook5.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Even Even Even More Pumpkins</p>
    </div>
        <div>
      <img src="../assets/images/spook6.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Rawr</p>
    </div>
        <div>
      <img src="../assets/images/spook7.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Murder mystery</p>
    </div>
        <div>
      <img src="../assets/images/spook8.png" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">The Exorcist</p>
    </div>
        <div>
      <img src="../assets/images/spook9.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">How to eat 3 apples in parallel </p>
    </div>
        <div>
      <img src="../assets/images/spook10.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">UFO spotting</p>
    </div>
        <div>
      <img src="../assets/images/spook11.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Tribe Leader Cao</p>
    </div>
        <div>
      <img src="../assets/images/spook12.jpg" alt="Spook 1" class="gallery-image">
      <p class="gallery-caption">Autumn Painting</p>
  </div> 
</div>

<script>
  function showGallery(galleryName) {
    const tabs = document.querySelectorAll('.tab');
    tabs.forEach(tab => tab.classList.remove('active'));

    const galleries = document.querySelectorAll('.gallery-container');
    galleries.forEach(gallery => gallery.classList.remove('active'));

    const selectedTab = document.querySelector(`[onclick="showGallery('${galleryName}')"]`);
    const selectedGallery = document.querySelector(`#${galleryName}-gallery`);

    selectedTab.classList.add('active');
    selectedGallery.classList.add('active');
  }
</script>
