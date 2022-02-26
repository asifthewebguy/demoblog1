<template>
  <div>
    <Header />
    <div class="container z-0 grid grid-cols-1 mx-auto divide-y-2 sm:mx-0 md:w-md">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
import MAC from '~/components/MAC.vue'
import Navigation from '~/components/Navigation.vue'
import Header from '../components/Header.vue'
export default {
  components: { MAC, Navigation, Header },
}
</script>
