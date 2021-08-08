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
    title: 'Riot Client',
    titleTemplate: '%s | In development',
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
