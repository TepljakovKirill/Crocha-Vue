<script setup>
import style from './categoryes.module.scss'


const categoryLinks = [
  { title: 'Одежда', url: '/cloth' },
  { title: 'Обувь', url: '/shoes' },
  { title: 'Аксессуары', url: '/accessories' },
  { title: 'Скидки', url: '/discounts' },
]
</script>

<template>
  <div class="wrapper">
    <div :class="style.container">
      <ul :class="style.categoryes__list">
        <li v-for="(link, index) in categoryLinks" :key='index'>
          <a :href="link.url" :class='style.categoryes__link'>{{ link.title }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

