<template>
  <div class="relative bg-white pt-4 pb-4 px-4 sm:px-6 lg:pt-8 lg:pb-8 lg:px-8">
    <div class="absolute inset-0">
      <div class="bg-white h-1/3 sm:h-2/3"></div>
    </div>
    <div class="relative max-w-7xl mx-auto mt-4 sm:mt-12 grid gap-5 max-w-lg mx-auto lg:grid-cols-3 lg:max-w-none">
      <!-- <div class="text-center">
        <h2 class="text-3xl leading-9 tracking-tight font-extrabold text-gray-900 sm:text-4xl sm:leading-10">
          From the blog
        </h2>
        <p class="mt-3 max-w-2xl mx-auto text-xl leading-7 text-gray-500 sm:mt-4">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa libero labore natus atque, ducimus sed.
        </p>
      </div> -->

      <article-card v-for="article in articles" :key="article.id" :article="article" />
    </div>
  </div>
</template>

<script>
import ArticleCard from '~/components/ArticleCard.vue'

export default {
  components: {
    ArticleCard
  },
  props: {
    articles: {
      type: Array,
      required: true
    }
  }
}
</script>

<style></style>
