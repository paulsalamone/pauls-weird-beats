<template>
  <div class="b-wrapper">
    <RouterView />
    <footer>c. 2023 pwb inc</footer>
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
// import MobileNav from './components/MobileNav.vue'
</script>

<style scoped>
.b-wrapper {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
