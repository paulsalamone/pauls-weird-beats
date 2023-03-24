<template>
  <div>
    <header>
      <TopNav />
      <!-- <MobileNav /> -->
      <HeroHeader />
    </header>
    <main>
      <!-- product list -->
      <ProductList :data="data" />
    </main>
    <!-- <p>{{ data.products }}</p> -->
  </div>
</template>


<script setup>
import HeroHeader from '../components/HeroHeader.vue'
import TopNav from '../components/TopNav.vue'
import ProductList from '../components/ProductList.vue'

import { ref, onMounted } from 'vue'
import axios from 'axios'

// const data = ref([])
// const URL = 'https://api.gumroad.com/v2/products'
// const ACCESS_TOKEN = import.meta.env.VITE_ACCESS_TOKEN
// console.log(ACCESS_TOKEN)
// onMounted(async () => {
//   try {
//     const response = await axios.get(URL, {
//       headers: {
//         Authorization: `Bearer ${ACCESS_TOKEN}`
//       }
//     })

//     data.value = response.data
//     console.log(data.value)
//   } catch (error) {
//     console.error(error)
//   }
// })

const data = {
  success: true,
  products: [
    {
      name: 'Kreuzberg Nights',
      preview_url:
        'https://public-files.gumroad.com/variants/tdjitk2zv0yztyqrk6qcq5zb5fx9/ae665e0ac58b5ad57c2ebb5e7f4e4c28854f779463935b9b94472f2b40d3134d',
      description: 'Hot techno loops for cool headz.',
      customizable_price: false,
      require_shipping: false,
      custom_receipt: '',
      custom_permalink: 'dirtynoise',
      subscription_duration: null,
      id: 'uT-Xk_2hN7OI5PJz9_w31g==',
      url: null,
      price: 500,
      currency: 'eur',
      short_url: 'https://paulsweirdbeats.gumroad.com/l/dirtynoise',
      thumbnail_url: null,
      tags: [],
      formatted_price: '€5',
      published: true,
      shown_on_profile: true,
      file_info: {},
      max_purchase_count: null,
      deleted: false,
      custom_fields: [],
      custom_summary: 'some samples',
      is_tiered_membership: false,
      recurrences: null,
      variants: [],
      sales_count: 0,
      sales_usd_cents: 0
    },
    {
      name: 'Rhymekölln',
      preview_url:
        'https://public-files.gumroad.com/variants/tdjitk2zv0yztyqrk6qcq5zb5fx9/ae665e0ac58b5ad57c2ebb5e7f4e4c28854f779463935b9b94472f2b40d3134d',
      description: 'Rap it up, Berlin ghetto-style.',
      customizable_price: false,
      require_shipping: false,
      custom_receipt: '',
      custom_permalink: 'dirtynoise',
      subscription_duration: null,
      id: 'uT-Xk_2hN7OI5PJz9_w31g==',
      url: null,
      price: 500,
      currency: 'eur',
      short_url: 'https://paulsweirdbeats.gumroad.com/l/dirtynoise',
      thumbnail_url: null,
      tags: [],
      formatted_price: '€5',
      published: true,
      shown_on_profile: true,
      file_info: {},
      max_purchase_count: null,
      deleted: false,
      custom_fields: [],
      custom_summary: 'some samples',
      is_tiered_membership: false,
      recurrences: null,
      variants: [],
      sales_count: 0,
      sales_usd_cents: 0
    },
    {
      name: 'Ich bin Nerdliner',
      preview_url:
        'https://public-files.gumroad.com/variants/tdjitk2zv0yztyqrk6qcq5zb5fx9/ae665e0ac58b5ad57c2ebb5e7f4e4c28854f779463935b9b94472f2b40d3134d',
      description: 'IDM with a teutonic saltiness',
      customizable_price: false,
      require_shipping: false,
      custom_receipt: '',
      custom_permalink: 'dirtynoise',
      subscription_duration: null,
      id: 'uT-Xk_2hN7OI5PJz9_w31g==',
      url: null,
      price: 500,
      currency: 'eur',
      short_url: 'https://paulsweirdbeats.gumroad.com/l/dirtynoise',
      thumbnail_url: null,
      tags: [],
      formatted_price: '€5',
      published: true,
      shown_on_profile: true,
      file_info: {},
      max_purchase_count: null,
      deleted: false,
      custom_fields: [],
      custom_summary: 'some samples',
      is_tiered_membership: false,
      recurrences: null,
      variants: [],
      sales_count: 0,
      sales_usd_cents: 0
    }
  ]
}
</script>

<style lang="css">
</style>

