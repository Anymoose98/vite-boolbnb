  <script>
  export default {
    data() {
      return {
        activeImage: 0,
        slides: [
          { image: '/slide-1.jpg' },
          { image: '/slide-2.jpg' },
          { image: '/slide-3.jpg' },
          { image: '/slide-4.jpg' },
          { image: '/slide-5.webp' },
        ]
      };
    },
    methods: {
      nextImg() {
        if (this.activeImage === this.slides.length - 1) {
          this.activeImage = 0;
        } else {
          this.activeImage++;
        }
      },
      prevImg() {
        if (this.activeImage === 0) {
          this.activeImage = this.slides.length - 1;
        } else {
          this.activeImage--;
        }
      },
      setImg(index) {
        this.activeImage = index;
      },
      startAutoPlay() {
        setInterval(() => {
          this.nextImg();
        }, 3000);
      }
    },
    created() {
      this.startAutoPlay();
    }
  };
  </script>
<template>
<div class="relative">
    <div class="carousel">
      <img v-for="(slide, index) in slides" 
           :src="slide.image" 
           :key="index" 
           @click="setImg(index)" 
           :class="{ active: index === activeImage }" 
           class="sfondo" 
           :style="{ display: index === activeImage ? 'block' : 'none' }" 
           alt="slider" />
    </div>
</div>
  
    <!-- Contenuto -->
    <div class="container">
      <div class="row">
      </div>
    </div>
  </template>
  
  
  <style scoped>
.relative {
  position: relative;
}

.carousel {
  display: flex;
  justify-content: center;
}

.carousel img {
  width: 100%;
  height: calc(100vh - 81px); /* Dimensioni delle immagini */
  object-fit: cover;
  object-position: center;
}

.carousel img:not(.active) {
  display: none; /* Nascondi le immagini non attive */
}
  </style>
  