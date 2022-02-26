<template>
  <header
    class="sticky top-0 z-50 flex justify-between w-full bg-white shadow-md sm:justify-center sm:flex-col md:flex-col"
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
