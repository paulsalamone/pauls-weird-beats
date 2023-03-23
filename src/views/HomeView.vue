<template>
  <main>
    <h1 v-html="title"></h1>
    <!-- <h2>{{ arr }}</h2> -->
    <!-- <h2>{{ output }}</h2> -->

    <h3>Coming soon...</h3>
  </main>
</template>


<script setup>
import { ref, computed } from 'vue'

const title = ref('')

const titleOrig = "Paul's Weird Beats"
const arr = titleOrig.split('')
arr.map((e) => {
  title.value += `<span style="font-size: ${r()}px">${e}</span>`
})

console.log(title.value)

function r() {
  return Math.floor(Math.random() * 40) + 40
}
</script>

