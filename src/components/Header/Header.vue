<script setup>
import style from './header.module.scss'
import CartIcon from '@/assets/icons/cart.svg'
import logo from '@/assets/icons/logo.png'

const menuLinks = [
  { title: 'Оплата и доставка', url: '/payment' },
  { title: 'Отзывы', url: '/reviews' }
]
</script>

<template>
  <div :class="style.header">
    <div class="wrapper">
      <div :class="style.container">
        <ul :class="style.menu">
          <li v-for="(link, index) in menuLinks" :key='index' :class='style.menu__list'>
            <a :href="link.url" :class='style.menu__link'>{{ link.title }}</a>
          </li>
        </ul>
        <a href="#" :class="style.logoLink">
          <img :src="logo" alt="Логотип">
        </a>
        <a href="#">
          <CartIcon :class="style.cartIcon" />
        </a>
      </div>
    </div>
  </div>
</template>

