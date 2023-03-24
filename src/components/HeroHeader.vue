<template>
  <div class="b-header">
    <img class="b-header__image" src="" alt="" />
    <div class="b-header__title" v-html="title1"></div>
    <div class="b-header__title" v-html="title2"></div>
    <!-- <h1>PWB</h1> -->
    <p>Odd loops and strange samples. Made in Berlin.</p>
    <h3></h3>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const title1 = ref('')
const title2 = ref('')

const titleOrig1 = "Paul's Weird"
const titleOrig2 = 'Beats'
const arr1 = titleOrig1.split('')
const arr2 = titleOrig2.split('')

// setInterval(() => {
//   title.value = ''
//   arr.map((e) => {
//     title.value += `<p style="font-size: ${r()}px; transform: rotate(${r2()}deg); color: lightgrey; ">${e}</p>`
//   })
// }, 100)

arr1.map((e) => {
  title1.value += `<div class=".b-header__title-letter" style="font-size: ${r()}px; transform: rotate(${r2()}deg); color: lightgrey; ">${e}</div>`
})

arr2.map((e) => {
  title2.value += `<div class=".b-header__title-letter" style="font-size: ${r()}px; transform: rotate(${r2()}deg); color: lightgrey; ">${e}</div>`
})

function r() {
  return Math.floor(Math.random() * 1.3) + 50
}
function r2() {
  return Math.floor(Math.random() * 15) - 5
}
</script>

<style lang="css">
.b-header {
  margin: 0.2rem;
  padding: 1rem 1rem;
  border-radius: 2rem;
  box-shadow: 0 0 10px grey;
  background: white;
}

.b-header__image {
  width: 100%;
  height: 200px;
  background-color: grey;
}
.b-header__title {
  transition: font-size 0.5s;
  display: flex;
  flex-direction: row;
  margin: 0px;
  padding: 0px;
}
.b-header__title-letter {
  margin: 0;
  padding: 0;
}

p {
  transition: rotate 200ms, opacity 200ms;
}
</style>