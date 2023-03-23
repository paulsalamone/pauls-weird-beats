<template>
  <header>
    <div class="wrapper">
      <TopNav />
    </div>
  </header>
  <main>
    <RouterView />

    DATA: {{ data }}
  </main>
</template>

<script setup>
// import { RouterView } from 'vue-router'
import TopNav from './components/TopNav.vue'
import { ref, onMounted } from 'vue'
import axios from 'axios'

const data = ref([])
const URL = 'https://api.gumroad.com/v2/products'
const ACCESS_TOKEN = import.meta.env.VITE_ACCESS_TOKEN
console.log(ACCESS_TOKEN)
onMounted(async () => {
  try {
    const response = await axios.get(URL, {
      headers: {
        Authorization: `Bearer ${ACCESS_TOKEN}`
      }
    })

    data.value = response.data
  } catch (error) {
    console.error(error)
  }
})
</script>

<style scoped>
</style>
