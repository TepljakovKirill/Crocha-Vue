<script setup>
import { onMounted, ref } from 'vue';
import axios from 'axios';
import Header from './components/Header/Header.vue'
import Categoryes from './components/Categoryes/Categoryes.vue';
import Slider from './components/Slider/Slider.vue';
import Stock from './components/Stock/Stock.vue';

const items = ref([])

const fetchItems = async () => {
    try {
     const { data } = await axios.get(`https://553829683cf71a20.mokky.dev/stock`)
     items.value = data
  } catch (err) {
    console.log(err)
  }
}

onMounted(fetchItems)

</script>

<template>
  <Header />

  <main>
    <Categoryes />
    <Slider />
    <Stock :items='items'/>
  </main>
</template>

<style scoped>
</style>
