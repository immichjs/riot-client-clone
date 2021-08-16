<template>
  <div class="login-container">
    <div class="helper-container">
      <div>
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" style="fill: #bbb;transform: ;msFilter:;"><path d="M12 2C6.486 2 2 6.486 2 12s4.486 10 10 10 10-4.486 10-10S17.514 2 12 2zm1 16h-2v-2h2v2zm.976-4.885c-.196.158-.385.309-.535.459-.408.407-.44.777-.441.793v.133h-2v-.167c0-.118.029-1.177 1.026-2.174.195-.195.437-.393.691-.599.734-.595 1.216-1.029 1.216-1.627a1.934 1.934 0 0 0-3.867.001h-2C8.066 7.765 9.831 6 12 6s3.934 1.765 3.934 3.934c0 1.597-1.179 2.55-1.958 3.181z"></path></svg>
        <div>
          <p>Você não precisa mais selecionar uma região antes de fazer login. Quando fizer login, a região associada à sua conta será atualizada com automaticamente.</p>
          <p>Se estiver com problemas para fazer login, talvez precise <a href="#">atualizar sua conta</a>.</p>
        </div>
      </div>
    </div>

    <div class="top-container">
      <img src="@/assets/svg/lol-logo.svg">
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
        <svg v-if="passwordType === 'password'" class="password-status" @click="changePassowordType" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: rgba(0, 0, 0, 1);transform: ;msFilter:;"><path d="M12 5c-7.633 0-9.927 6.617-9.948 6.684L1.946 12l.105.316C2.073 12.383 4.367 19 12 19s9.927-6.617 9.948-6.684l.106-.316-.105-.316C21.927 11.617 19.633 5 12 5zm0 11c-2.206 0-4-1.794-4-4s1.794-4 4-4 4 1.794 4 4-1.794 4-4 4z"></path><path d="M12 10c-1.084 0-2 .916-2 2s.916 2 2 2 2-.916 2-2-.916-2-2-2z"></path></svg>
        <svg v-if="passwordType === 'text'" class="password-status" @click="changePassowordType" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: rgba(0, 0, 0, 1);transform: ;msFilter:;"><path d="M8.073 12.194 4.212 8.333c-1.52 1.657-2.096 3.317-2.106 3.351L2 12l.105.316C2.127 12.383 4.421 19 12.054 19c.929 0 1.775-.102 2.552-.273l-2.746-2.746a3.987 3.987 0 0 1-3.787-3.787zM12.054 5c-1.855 0-3.375.404-4.642.998L3.707 2.293 2.293 3.707l18 18 1.414-1.414-3.298-3.298c2.638-1.953 3.579-4.637 3.593-4.679l.105-.316-.105-.316C21.98 11.617 19.687 5 12.054 5zm1.906 7.546c.187-.677.028-1.439-.492-1.96s-1.283-.679-1.96-.492L10 8.586A3.955 3.955 0 0 1 12.054 8c2.206 0 4 1.794 4 4a3.94 3.94 0 0 1-.587 2.053l-1.507-1.507z"></path></svg>
      </div>

      <div class="other-accesses">
        <div>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: #fff;transform: ;msFilter:;"><path d="M13.397 20.997v-8.196h2.765l.411-3.209h-3.176V7.548c0-.926.258-1.56 1.587-1.56h1.684V3.127A22.336 22.336 0 0 0 14.201 3c-2.444 0-4.122 1.492-4.122 4.231v2.355H7.332v3.209h2.753v8.202h3.312z"></path></svg>
        </div>
        <div>
          <img src="@/assets/images/google-logo.png" width="24">
        </div>
        <div>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: #fff;transform: ;msFilter:;"><path d="M19.665 16.811a10.316 10.316 0 0 1-1.021 1.837c-.537.767-.978 1.297-1.316 1.592-.525.482-1.089.73-1.692.744-.432 0-.954-.123-1.562-.373-.61-.249-1.17-.371-1.683-.371-.537 0-1.113.122-1.73.371-.616.25-1.114.381-1.495.393-.577.025-1.154-.229-1.729-.764-.367-.32-.826-.87-1.377-1.648-.59-.829-1.075-1.794-1.455-2.891-.407-1.187-.611-2.335-.611-3.447 0-1.273.275-2.372.826-3.292a4.857 4.857 0 0 1 1.73-1.751 4.65 4.65 0 0 1 2.34-.662c.46 0 1.063.142 1.81.422s1.227.422 1.436.422c.158 0 .689-.167 1.593-.498.853-.307 1.573-.434 2.163-.384 1.6.129 2.801.759 3.6 1.895-1.43.867-2.137 2.08-2.123 3.637.012 1.213.453 2.222 1.317 3.023a4.33 4.33 0 0 0 1.315.863c-.106.307-.218.6-.336.882zM15.998 2.38c0 .95-.348 1.838-1.039 2.659-.836.976-1.846 1.541-2.941 1.452a2.955 2.955 0 0 1-.021-.36c0-.913.396-1.889 1.103-2.688.352-.404.8-.741 1.343-1.009.542-.264 1.054-.41 1.536-.435.013.128.019.255.019.381z"></path></svg>
        </div>
      </div>

      <div class="keep-login">
        <input type="checkbox" id="keep-login">
        <label for="keep-login">Manter login</label>
      </div>
      
      <div class="login-button" :class="activeLoginButton ? 'active-login-button' : ''">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: #e8e8e8;transform: ;msFilter:;"><path d="m11.293 17.293 1.414 1.414L19.414 12l-6.707-6.707-1.414 1.414L15.586 11H6v2h9.586z"></path></svg>
      </div>

      <div class="account-stuations">
        <a href="#">Não consegue iniciar sessão?</a>
        <a href="#">Criar conta</a>
      </div>

      <div class="version">
        <p>V36.0.2</p>
      </div>
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
        if (this.user.username.trim().length >= 2 && this.user.password.trim()) {
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
