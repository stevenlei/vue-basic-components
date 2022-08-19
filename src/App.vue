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
      ],
      selectedProducts: [],
    }
  },
  methods: {
    handleChange(newSelectedProducts) {
      this.selectedProducts = newSelectedProducts;
    }
  }
}
</script>

<template>
  <div class="min-h-screen bg-slate-100 flex justify-center items-center">
    <div class="max-w-5xl mx-auto flex flex-1 gap-x-8">
      <div class="flex-1">
        <h2 class="text-3xl font-bold mb-6">Apple Products</h2>
        <List :products="products" @change="handleChange" />
      </div>
      <div class="flex-1">
        <h2 class="text-3xl font-bold mb-6 text-slate-400">Selected Products</h2>
        <p class="text-2xl text-slate-600">{{ selectedProducts.map(selected => selected.name).join(', ') || 'Nothing yet' }}</p>
      </div>
    </div>
  </div>
</template>
