<template>
  <header>
    <div class="wrapper">
      <TopNav />
    </div>
  </header>
  <main><RouterView /></main>
</template>

<script setup>
import { RouterView } from 'vue-router'
import TopNav from './components/TopNav.vue'
</script>

<style scoped>
</style>
