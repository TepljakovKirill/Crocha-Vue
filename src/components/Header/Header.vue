<script setup>
import style from './header.module.scss'
</script>

<template>
  <div :class="style.header">
    <div class="wrapper">
      <div :class="title"><h1>Это заголовок</h1></div>
    </div>
  </div>
</template>

