<script setup>
import style from './stock.module.scss'
import ProductCard from '../ProductCard/ProductCard.vue';

defineProps({
  items: Array
})


</script>

<template>
  <div :class="style.stock">
    <div class="wrapper">
        <div class="border">
          <div :class="style.stock_container">
            <h2 class='title-section'>Акции</h2>
            <div :class="style.stock_wrapper">
              <ProductCard
                v-for='item in items'
                :key='item.id'
                :type='item.type'
                :imageUrl='item.imageUrl'
                :title='item.title'
                :price='item.price'
                :oldPrice='item.oldPrice'
                :discount='item.discount'
                :discountValue='item.discountValue'
              />
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

