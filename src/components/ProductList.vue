<template>
  <div>
    product list:

    <ProductListItem v-for="product in props.data.products" :key="product.id" :product="product" />

    <p>{{ props.data.products }}</p>
  </div>
</template>

<script setup>
import ProductListItem from '../objects/ProductListItem.vue'

const props = defineProps({ data: Object })

const fakes = [
  {
    id: 'pwb_001',
    title: 'Kreuzberg Nights',
    type: 'loops',
    genre: 'techno',
    price: '5',
    description:
      'Grotty synth loops filtered through a bunch of pedals. Gritty noise for hot summer nights spent spitting on the Bürgersteig.'
  },
  {
    id: 'pwb_002',
    title: 'Bowie Allee',
    type: 'samples',
    genre: 'pop',
    price: '7',
    description:
      'A handful of chord one-hits, gated reverb drums, cymbals, and vocal shrieks perfect for the pop experimentalist.'
  },
  {
    id: 'pwb_003',
    title: 'Brutalist Drums',
    type: 'samples',
    genre: 'rap',
    price: '4',
    description:
      "Classic Roland 808 beats filtered through a patented blend of stolen guitar pedals. Kick rhymes over broken glass and don't look back."
  }
]
</script>

<style>
li {
  list-style-type: none;
}
</style>