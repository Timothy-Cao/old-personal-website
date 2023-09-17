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
</style>

<div class="tab-container">
  <div class="tab active" onclick="showGallery('rabbit')">Rabbit Gallery</div>
  <div class="tab" onclick="showGallery('photography')">Photography Gallery</div>
  <div class="tab" onclick="showGallery('monthly')">Monthly Gallery</div>
  <div class="tab" onclick="showGallery('AI')">AI Gallery</div>
</div>

<div class="gallery-container active" id="rabbit-gallery">
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
      <div>
      <img src="../assets/images/photography1.png" alt="photography1" class="gallery-image">
      <p class="gallery-caption">Photo by Angus Lai</p>
    </div>
    <div>
      <img src="../assets/images/photography2.jpg" alt="photography2" class="gallery-image">
      <p class="gallery-caption">Photo by Image.Rosie</p>
    </div>
    <div>
      <img src="../assets/images/photography3.jpg" alt="photography3" class="gallery-image">
      <p class="gallery-caption">Photo by Image.Rosie</p>
    </div>
  </div>
</div>

<div class="gallery-container" id="monthly-gallery">
  <h1 class="gallery-title">Seasonal Pics (Summer 23)</h1>
  <div class="gallery-table">
    <div>
      <img src="../assets/images/summer1.jpeg" alt="summer1" class="gallery-image">
      <p class="gallery-caption">Cast us for your next horror movie</p>
    </div>
    <div>
      <img src="../assets/images/summer3.jpg" alt="summer2" class="gallery-image">
      <p class="gallery-caption">Pinkies up!</p>
    </div>
    <div>
      <img src="../assets/images/summer6.jpg" alt="summer3" class="gallery-image">
      <p class="gallery-caption">I'm something of a celebrity myself</p>
    </div>
    <div>
      <img src="../assets/images/summer2.jpg" alt="summer4" class="gallery-image">
      <p class="gallery-caption">I'm actually 100ft in the air</p>
    </div>
    <div>
      <img src="../assets/images/summer4.jpg" alt="summer5" class="gallery-image">
      <p class="gallery-caption">Creatures of the night</p>
    </div>
    <div>
      <img src="../assets/images/summer5.jpg" alt="summer6" class="gallery-image">
      <p class="gallery-caption">(Physical) Labour of love</p>
    </div>
  </div>
</div>

<div class="gallery-container" id="AI-gallery">
  <h1 class="gallery-title">AI Gallery</h1>
  <div class="gallery-table">
    <div>
      <img src="../assets/images/ai1.jpg" alt="AI 1" class="gallery-image">
      <p class="gallery-caption">Generated with Remini</p>
    </div>
    <div>
      <img src="../assets/images/ai2.jpg" alt="AI 2" class="gallery-image">
      <p class="gallery-caption">Generated with Remini</p>
    </div>
    <div>
      <img src="../assets/images/ai3.jpg" alt="AI 3" class="gallery-image">
      <p class="gallery-caption">Generated with Remini</p>
    </div>
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
