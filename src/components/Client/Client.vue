<template>
  <div class="client-container">
    <Login />
    <div class="temp">
      <Main />
    </div>
  </div>
</template>

<script>
import Login from '../Login/Login'
import Main from '../Main/Main'
export default {
  components: {
    Login,
    Main,
  }

}
</script>

<style src="./style.scss" lang="scss" scoped />
