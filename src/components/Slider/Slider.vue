<script setup>
import Slide1 from '@/assets/images/bunner/bunner.png'
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';
import '@/assets/styles/swiper-custom.scss'
import style from './slider.module.scss'

const modules = [Autoplay, Pagination];

</script>

<template>
  <div class="wrapper">
    <div :class="style.container">
      <swiper
        :modules="modules"
        :slides-per-view="1"
        :space-between="20"
        :autoplay="{
          delay: 3000,
          disableOnInteraction: false,
        }"
        :pagination="{
          clickable: true,
          dynamicBullets: false
        }"
        :loop="true"
        :grab-cursor="true"
        :centered-slides="false"
        :speed="800"
      >
        <swiper-slide>
          <img :src="Slide1" alt="Картинка">
        </swiper-slide>
        <swiper-slide>
          <img :src="Slide1" alt="Картинка">
        </swiper-slide>
        <swiper-slide>
          <img :src="Slide1" alt="Картинка">
        </swiper-slide>
        <swiper-slide>
          <img :src="Slide1" alt="Картинка">
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
