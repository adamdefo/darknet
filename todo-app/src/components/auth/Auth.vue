<template>
    <div class="auth">
        <div class="auth__container">
            <form @submit.prevent="onSubmit" class="auth__form">
                <div class="auth__group">
                    <div class="auth__group-item">
                        <input v-model="login" class="auth__control" type="text" name="login" />
                    </div>
                    
                </div>
                <div class="auth__group-item">
                    <div class="auth__group-item">
                        <button @click="signIn" class="auth__button" type="button">
                            <span>Login</span>
                        </button>
                    </div>
                </div>
            </form>
        </div>
        

    </div>
</template>

<script>
export default {
  name: 'Auth',
  props: {},
  model: {
    login: {
      type: Number,
      default: 0
    }
  },
  data () {
    return {
      login: ''
    }
  },
  methods: {
    signIn: function (event) {
      alert(this.login)
    },
    onSubmit: function (event) {
      alert('Submit')
    }
  }
}
</script>

<style lang="scss" scoped>
.auth {
  position: relative;
  width: 100%;
  min-width: 300px;
  max-width: 460px;
  &__container {
    padding: 20px;
  }
  &__form {
      position: relative;
  }
}
</style>