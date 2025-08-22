<script setup>
import style from './productCard.module.scss'
import image from '@/assets/images/card-1.jpg'
</script>

<template>
  <div :class="style.productCard">
    <img :src="image" alt="Картинка">
    <div :class="style.productCard_description">
      <span :class="style.productCard_title">Костюм для девочки</span>
      <div :class="style.price_block">
        <span :class='style.price'>599 ₽</span>
        <span :class='style.price_old'>719 ₽</span>
      </div>
      <div :class="style.productCard_block_button">
        <button :class="style.view_button">Смотреть</button>
        <button :class="style.cart_button">В корзину</button>
      </div>
    </div>
  </div>
</template>
