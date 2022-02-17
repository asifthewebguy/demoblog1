<template>
  <nav class="flex justify-between items-center">
    <ul>
      <li class="list-none inline-block mx-4">
        <nuxt-link to="/">
          <i class="icon icon-home" aria-hidden="true"></i>
        </nuxt-link>
      </li>
      <li class="list-none inline-block mx-4">
        <nuxt-link to="about">About</nuxt-link>
      </li>
      <li class="list-none inline-block mx-4">
        <nuxt-link to="work">Work</nuxt-link>
      </li>
      <li class="list-none inline-block mx-4">
        <nuxt-link to="contact">Contact</nuxt-link>
      </li>
      <li class="list-none inline-block mx-4">
        <nuxt-link to="resume">Resume</nuxt-link>
      </li>
      <li class="list-none inline-block mx-4">
        <i class="icon icon-moon" aria-hidden="true"></i>
      </li>
      <!-- <router-link
        to="resume"
        custom
        v-slot="{ href, route, navigate, isActive, isExactActive }"
      >
        <li
          :class="[
            isActive && 'router-link-active',
            isExactActive && 'router-link-exact-active',
          ]"
        >
          <a :href="href" @click="navigate">{{ route.name }}</a>
        </li>
      </router-link> -->
    </ul>
  </nav>
</template>

<script>
export default {}
</script>

<style scoped>
/* horizontal navigation */

.icon {
  @apply inline-block w-4 h-4 bg-contain  bg-no-repeat;
}

.icon-home {
  background-image: url('~assets/svg/house.svg');
}

.icon-moon {
  background-image: url('~assets/svg/moon.svg');
}
</style>
