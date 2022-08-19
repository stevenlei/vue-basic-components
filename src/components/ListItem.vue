<script>
export default {
  props: ['name', 'selectedItem', 'unselectedItem'],
  data() {
    return {
      isClicked: false,
    }
  },
  methods: {
    onClick() {
      // update the data property
      this.isClicked = !this.isClicked;

      // let parent knows that the item has been clicked
      if (this.isClicked) {
        this.$emit('selectedItem');
      } else {
        this.$emit('unselectedItem');
      }
    }
  }
}
</script>

<template>
  <li
    class="rounded-xl bg-white p-6 shadow-md w-full hover:scale-105 hover:shadow-lg transition"
    :class="{'bg-slate-800 text-white': isClicked}"
    @click="onClick"
  >
    {{ name }}
  </li>
</template>