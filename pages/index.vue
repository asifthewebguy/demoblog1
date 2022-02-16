<template>
  <div class="container">
    <div class="container flex mx-auto">
      <div class="about max-w-2/3">
        <h2>{{ homePage.author }}</h2>
        <nuxt-content :document="homePage" />
      </div>
      <div class="img max-w-1/3">
        <img :src="homePage.img" alt="" />
      </div>
    </div>
    <div>
      <h1>Blog Posts</h1>
      <ul>
        <li v-for="article of articles" :key="article.slug">
          <!-- <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }"> -->
          <NuxtLink
            :to="{ name: 'article-slug', params: { slug: article.slug } }"
          >
            <img :src="require(`~/assets/images/${article.img}`)" />
            <div>
              <h2>{{ article.title }}</h2>
              <p>by {{ article.author.name }}</p>
              <p>{{ article.description }}</p>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({ $content, params }) {
    const homePage = await $content('page', 'home-page').fetch()
    const articles = await $content('articles')
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'asc')
      .fetch()
    return {
      homePage,
      articles,
    }
  },
}
</script>
