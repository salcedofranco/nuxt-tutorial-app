<template>
  <section class="home">
    <h1 class="home__heading">About Nuxtjs Directory Structure</h1>
    <div class="directories">
      <div class="directory__container" v-for="directory in directories" :key="directory.id">
        <p class="directory__name">
          <nuxt-link
            :to="{ name: 'id', params: { id: directory.id, dir: directory } }"
          >{{ directory.name }}</nuxt-link>
        </p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "about-nuxt",
  data() {
    return {
      directories: [
        {
          id: 0,
          name: "CERO 000000",
          info:
            "By default, Nuxt uses vue-loader, file-loader and url-loader webpack loaders for strong assets serving. You can also use the static directory for static assets. This folder is for un-compiled files such as images, font files, SASS, LESS or JavaScript files"
        },
        {
          id: 1,
          name: "UNO 111111",
          info:
            "The components directory contains your Vue.js Components. You can’t use asyncData in these components."
        },
        {
          id: 2,
          name: "DOS 2222222",
          info:
            "The layouts directory includes your application layouts. Layouts are used to change the look and feel of your page (for example by including a sidebar). Layouts are a great help when you want to change the look and feel of your Nuxt.js app. Whether you want to include a sidebar or having distinct layouts for mobile and desktop"
        },
        {
          id: 3,
          name: "TRES 3333333",
          info:
            "The middleware directory contains your Application Middleware. Middleware lets you define custom functions that can be run before rendering either a page or a group of pages (layouts)."
        }

      ]
    };
  }
};
</script>
<style>
</style>
