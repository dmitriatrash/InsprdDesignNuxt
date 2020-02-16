<template>
  <div class="container">
    <div>
      <Header />
      <logo />
      <h1 class="title">
        Insprd Design
      </h1>
      <!--<div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button&#45;&#45;green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button&#45;&#45;grey"
        >
          GitHub
        </a>
      </div>-->
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/Header.vue'
export default {
  components: {
    Logo,
    Header
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: url("https://cdn.pixabay.com/photo/2017/01/18/15/51/paper-1990111_1280.jpg") center no-repeat;
  background-size: cover;
}

.title {
  font-family: 'Playfair Display', serif;
  display: block;
  font-weight: 300;
  font-size: 5em;
  color: #121212;
  letter-spacing: 1px;
  margin: 1rem;
}

.subtitle {
  font-weight: 300;
  font-size: 3em;
  color: #343434;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
