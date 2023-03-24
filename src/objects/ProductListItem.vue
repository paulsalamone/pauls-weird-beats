<template>
  <div class="b-product-list-item">
    <img class="b-product-list-item__image" src="" alt="" />
    <h3>{{ p.name }}</h3>
    <p>
      {{ p.description }}
    </p>
    <p>{{ p.formatted_price }}</p>
    <!-- <button>ADD TO CART</button> -->
    <h4>Samples:</h4>
    <audio src="" controls>audio player</audio>
    <details>
      <summary>more</summary>
      <audio src="" controls>audio player</audio>
      <audio src="" controls>audio player</audio>
    </details>
  </div>
</template>

<script setup>
const props = defineProps({ product: Object })
const p = props.product
</script>

<style>
.b-product-list-item {
  border: 1px solid black;
  /* height: 100px; */
  border-radius: 0.5rem;
  margin: 0.25rem;
  padding: 0.3rem;
}

.b-product-list-item__image {
  height: 100px;
  width: 100%;
  background-color: grey;
}
</style>