<template>
  <nav class="b-mobile-nav">
    <RouterLink class="b-nav__link" to="/">Home</RouterLink>
    <RouterLink class="b-nav__link" to="/about">About</RouterLink>
    <RouterLink class="b-nav__link" to="/shop">Shop</RouterLink>
    <RouterLink class="b-nav__link" to="/shop">Your Cart</RouterLink>
    <RouterLink class="b-nav__link" to="/shop">Contact</RouterLink>
  </nav>
</template>

<script setup>
import { RouterLink } from 'vue-router'
import { ref } from 'vue'
</script>

<style>
</style>