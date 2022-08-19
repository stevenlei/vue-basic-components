<script>
export default {
  props: ['name'],
  data() {
    return {
      isClicked: false,
    }
  }
}
</script>

<template>
  <li
    class="rounded-xl bg-white p-6 shadow-md w-full hover:scale-105 hover:shadow-lg transition"
    :class="{'bg-slate-800 text-white': isClicked}"
    @click="isClicked = !isClicked"
  >
    {{ name }}
  </li>
</template>