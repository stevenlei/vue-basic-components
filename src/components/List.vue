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
  },
  data() {
    return {
      selectedItems: [],
    }
  },
  methods: {
    add(product) {
      this.selectedItems.push(product);
      this.$emit('change', this.selectedItems);
    },
    subtract(product) {
      this.selectedItems.splice(this.selectedItems.indexOf(product), 1);
      this.$emit('change', this.selectedItems);
    }
  }
}
</script>

<template>
  <ul class="flex flex-col gap-y-4 text-2xl text-slate-600">
    <ListItem
      v-for="product in products"
      :key="product.sku"
      :product="product"
      @selectedItem="add"
      @unselectedItem="subtract"
    />
  </ul>
  <p class="p-6 text-slate-500">{{ selectedItems.length }} item(s) selected</p>
</template>