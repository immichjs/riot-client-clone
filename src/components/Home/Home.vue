<template>
  <div class="home">
    <header @click="href('https://vuejs.org/')" title="Vue.js Docs">
      <img alt="Vue logo" src="../../assets/images/logo.png">
      <h1>{{ message }}</h1>
    </header>
    <nav>
      <ul>
        <li title="Vuex Docs" @click="href('https://vuex.vuejs.org/')">
          <img src="../../assets/images/vuex-logo.png">
          <span>Vuex</span>
        </li>
        <li title="Boxicons Docs" @click="href('https://boxicons.com/')">
          <img src="../../assets/images/boxicons-logo.png">
          <span>Boxicons</span>
        </li>
        <li title="Vue-meta Docs" @click="href('https://vue-meta.nuxtjs.org/')">
          <img src="../../assets/images/vue-meta-logo.png">
          <span>Vue-meta</span>
        </li>
        <li title="Sass Docs" @click="href('https://sass-lang.com/')">
          <img src="../../assets/images/sass-logo.png">
          <span>Sass</span>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
    message: String
  },
  methods: {
    href (url) {
      window.location.href = url
    }
  }
}
</script>

<style src="./style.scss" scoped lang="scss"></style>
