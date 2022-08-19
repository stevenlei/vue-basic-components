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
      itemsCount: 0,
    }
  },
  methods: {
    add() {
      this.itemsCount++;
    },
    subtract() {
      this.itemsCount--;
    }
  }
}
</script>

<template>
  <ul class="flex flex-col gap-y-4 text-2xl text-slate-600">
    <ListItem
      v-for="product in products"
      :key="product.sku"
      :name="product.name"
      @selectedItem="add"
      @unselectedItem="subtract"
    />
  </ul>
  <p class="p-6 text-slate-500">{{ itemsCount }} item(s) selected</p>
</template>