<template>
    <div class="carousel-container">
      <h2>Image Carousel</h2>
      <img :src="images[currentImage]" :alt="'Image ' + (currentImage + 1)" style="width: 300px; height: 200px;">
      <br>
          <div class="button-container">
      <button @click="prevImage" class="carousel-button">Previous</button>
      <button @click="nextImage" class="carousel-button">Next</button>
    </div>
          </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        images: [
          'https://picsum.photos/id/77/450/300',
          'https://picsum.photos/id/78/450/300',
          'https://picsum.photos/id/79/450/300',
        ],
        currentImage: 0,
      };
    },
    methods: {
      nextImage() {
        this.currentImage = (this.currentImage + 1) % this.images.length;
      },
      prevImage() {
        this.currentImage = (this.currentImage - 1 + this.images.length) % this.images.length;
      },
    },
  };
  </script>


  <style scoped>
  .carousel-container {
    text-align: center; 
  }
  .button-container {
    margin-top: 10px;
    display: flex;
    justify-content: center; 
    gap: 10px; 
  }
  
  .carousel-button {
    padding: 10px 20px; 
    background-color: #4CAF50; 
    color: white;
    border: none; 
    cursor: pointer; 
    border-radius: 5px; 
  }
  
  .carousel-button:hover {
    background-color: #45a049; 
  }
  </style>