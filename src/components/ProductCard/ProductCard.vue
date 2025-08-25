<script setup>
import style from './productCard.module.scss'
import image from '@/assets/images/card-1.jpg'
import Button from '../UI/Button.vue';

defineProps({
  id: Number,
  category: String,
  type: String,
  imageUrl: String,
  title: String,
  price: Number,
  oldPrice: Number,
  discount: Boolean,
  discountValue: Number,
})

const handleClick = () => {
  alert('Кнопка нажата!')
}
</script>

<template>
  <div :class="style.productCard">
    <img :src="image" alt="Картинка">
    <div :class="style.productCard_description">
      <span :class="style.productCard_title">{{ title }}</span>
      <div :class="style.price_block">
        <span :class='style.price'>{{ price }} ₽</span>
        <span :class='style.price_old'>{{ oldPrice }} ₽</span>
      </div>
      <div :class="style.productCard_block_button">
        <Button variant="blue" size="small" @click="handleClick">Смотреть</Button>
        <Button variant="white" size="small" @click="handleClick">В корзину</Button>
      </div>
    </div>
  </div>
</template>
