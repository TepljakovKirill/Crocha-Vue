<script setup>
import style from './stock.module.scss'
import ProductCard from '../ProductCard/ProductCard.vue';
</script>

<template>
  <div :class="style.stock">
    <div class="wrapper">
        <div class="border">
          <div :class="style.stock_container">
            <h2 class='title-section'>Акции</h2>
            <div :class="style.stock_wrapper">
              <ProductCard />
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

