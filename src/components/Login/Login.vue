<template>
  <div class="login-container">
    <div class="helper-container">
      <box-icon type='solid' name='help-circle' color="#bbb" size="20px"></box-icon>
    </div>

    <div class="top-container">
      <img src="@/assets/images/lol-logo.svg">
      <h1>Fazer login</h1>
    </div>

    <div class="form-login">
      <div>
        <input required='' type='text' v-model="user.username">
        <label alt="Nome de usuário" placeholder="Nome de usuário"></label>
      </div>
      <div>
        <input required='' :type='passwordType' v-model="user.password">
        <label alt="Senha" placeholder="Senha"></label>
        <box-icon name='hide' class="password-status" type='solid' color="#000" v-if="passwordType === 'password'" @click="changePassowordType"></box-icon>
        <box-icon name='show' class="password-status" type='solid'  color="#000" v-if="passwordType === 'text'" @click="changePassowordType"></box-icon>
      </div>

      <div class="other-accesses">
        <div>
         <box-icon name='facebook' type='logo' color="#fff"></box-icon>
        </div>
        <div>
          <img src="@/assets/images/google-logo.png" width="24">
        </div>
        <div>
          <box-icon name='apple' type='logo' color="#fff"></box-icon>
        </div>
      </div>

      <div class="keep-login">
        <input type="checkbox" id="keep-login">
        <label for="keep-login">Manter login</label>
      </div>
      
      <div class="login-button" :class="activeLoginButton ? 'active-login-button' : ''">
        <box-icon name='right-arrow-alt' size="32px" :color="activeLoginButton ? '#fff' : '#e8e8e8'"></box-icon>
      </div>

      <div class="account-stuations">
        <a href="#">Não consegue iniciar sessão?</a>
        <a href="#">Criar conta</a>
      </div>

      <p class="version">V36.0.2</p>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      user: { username: '', password: '' },
      activeLoginButton: false,
      passwordType: 'password',
    }
  },
  methods: {
    changePassowordType () {
      this.passwordType === 'password'
        ? this.passwordType = 'text'
        : this.passwordType = 'password'
    },
  },
  watch: {
    user: {
      deep: true,
      handler () {
        if (this.user.username.length >= 2 && this.user.password) {
          this.activeLoginButton = true
        } else {
          this.activeLoginButton = false
        }
      }
    }
  }
}
</script>

<style src="./style.scss" lang="scss" scoped />
