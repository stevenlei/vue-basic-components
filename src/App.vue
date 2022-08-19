<script>
import List from "./components/List.vue"

export default {
  components: {
    List,
  },
  data() {
    return {
      products: [
        {
          sku: 'iphone',
          name: 'iPhone',
        },
        {
          sku: 'ipad',
          name: 'iPad',
        },
        {
          sku: 'mac',
          name: 'Mac',
        },
        {
          sku: 'appletv',
          name: 'Apple TV',
        },
        {
          sku: 'homepod',
          name: 'HomePod',
        },
        
      ]
    }
  }
}
</script>

<template>
  <div class="min-h-screen bg-slate-100 flex justify-center items-center">
    <div class="max-w-sm mx-auto flex-1">
      <h2 class="text-3xl font-bold mb-6">Apple Products</h2>
      <List :products="products" />
    </div>
  </div>
</template>
