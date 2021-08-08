<template>
  <div class="client-container">
    <MenuBar />
    <div class="content">
      <Login />
      <Main />
    </div>
  </div>
</template>

<script>
import MenuBar from '../MenuBar/MenuBar'
import Login from '../Login/Login'
import Main from '../Main/Main'
export default {
  components: {
    MenuBar,
    Login,
    Main,
  }

}
</script>

<style src="./style.scss" lang="scss" scoped />
