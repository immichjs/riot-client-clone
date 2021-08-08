<template>
  <div id="app">
    <Client />
  </div>
</template>

<script>
// import components
import Client from '@/components/Client/Client'

export default {
  name: 'App',
  metaInfo: {
    title: 'League of Legends',
    titleTemplate: '%s | Client in development',
    htmlAttrs: {
      lang: 'pt-br',
      amp: true
    }
  },
  components: {
    Client
  }
}
</script>

<style src="./style.scss" lang="scss" />
