<template>
  <div id="app">
    <Home message="Bem-vindo a sua aplicação Vue.js"/>
    <footer>
      <p>Template made by Mich ❤</p>
    </footer>
  </div>
</template>

<script>
import Home from './components/Home/Home.vue'

export default {
  name: 'App',
  metaInfo: {
    title: 'Vue.js + Sass',
    titleTemplate: '%s | Template!',
    htmlAttrs: {
      lang: 'pt-br',
      amp: true
    }
  },
  components: {
    Home
  }
}
</script>

<style src="./style.scss" lang="scss" />
