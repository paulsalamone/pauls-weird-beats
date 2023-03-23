<template>
  <main>
    <h1 v-html="title"></h1>
    <h3>Coming soon...</h3>
  </main>
</template>


<script setup>
import { ref } from 'vue'

const title = ref('')
const titleOrig = "Paul's Weird Beats"
const arr = titleOrig.split('')
arr.map((e) => {
  title.value += `<span style="font-size: ${r()}px">${e}</span>`
})

function r() {
  return Math.floor(Math.random() * 40) + 40
}
</script>

