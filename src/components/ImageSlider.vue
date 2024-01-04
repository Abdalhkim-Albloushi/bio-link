<template>
<div class="image">
      
<vueper-slides :slide-ratio="3 / 7" autoplay :slide-content-outside="contentPosition">
  <vueper-slide
    v-for="(slide, i) in slides"
    :key="i"
    :image="slide.image"
    class="image-info"
    >
    <template #content>
      <div class="vueperslide__content-wrapper" style="flex-direction: row">
        <i class="material-icons"></i>
        <span>{{ slide.title }}</span>
      </div>
    </template>
  </vueper-slide>
</vueper-slides>
</div>
</template>

<script setup>

import MyImage1 from '../assets/img3.jpg'
import MyImage2 from '../assets/img1.webp'
import MyImag3 from '../assets/img2.webp'
import { VueperSlides, VueperSlide } from 'vueperslides'

const slides =  [
  {
    title: 'El Teide Volcano, Spain',
    content: 'Photo by Max Rive',
    // You can also provide a URL for the image.
    image:  MyImage1,
  },
  {
    title: 'El Teide Volcano, Spain',
    content: 'Photo by Max Rive',
    // You can also provide a URL for the image.
    image:  MyImage2,
  },
  {
    title: 'El Teide Volcano, Spain',
    content: 'Photo by Max Rive',
    // You can also provide a URL for the image.
    image:  MyImag3,
  },
  
 
]
</script>

<style>
.vueperslide--loading .vueperslide__content-wrapper {
  display: none !important;
}
/* If you want to hide the slide description while loading. */
.image{
    margin-top: 50px;
    border-radius: 5px;
}

.image-info{
    border-radius: 5px;

}
</style>