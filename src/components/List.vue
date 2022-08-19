<script>
import ListItem from "./ListItem.vue";

export default {
  components: {
    ListItem,
  },
  props: {
    products: {
      type: Array,
      required: true,
    },
  }
}
</script>

<template>
  <ul class="flex flex-col gap-y-4 text-2xl text-slate-600">
    <ListItem v-for="product in products" :key="product.sku" :name="product.name" />
  </ul>
</template>