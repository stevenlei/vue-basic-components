<script>
import ListItem from "./components/ListItem.vue"

export default {
  components: {
    ListItem
  }
}
</script>

<template>
  <div class="min-h-screen bg-slate-100 flex justify-center items-center">
    <div class="max-w-sm mx-auto flex-1">
      <h2 class="text-3xl font-bold mb-6">Apple Products</h2>
      <ul class="flex flex-col gap-y-4 text-2xl text-slate-600">
        <list-item name="iPhone" />
      </ul>
    </div>
  </div>
</template>
