<template>
  <header
    class="flex justify-around w-full shadow-md sm:justify-center sm:flex-col md:flex-col"
  >
    <MAC />
    <Navigation />
  </header>
</template>

<script>
import MAC from './MAC.vue'
export default {
  components: { MAC },
}
</script>
