<script setup>
import style from './productCard.module.scss'
import image from '@/assets/images/card-1.jpg'
import Button from '../UI/Button.vue';

const handleClick = () => {
  alert('Кнопка нажата!')
}
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
        <Button variant="blue" size="small" @click="handleClick">Смотреть</Button>
        <Button variant="white" size="small" @click="handleClick">В корзину</Button>
      </div>
    </div>
  </div>
</template>
