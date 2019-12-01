<template>
  <div>
    username: <input type="text" v-model="changer.name"/>
    <br/><br/>
    password: <input type="password" v-model="changer.password">
    <br/><br/>
    <button v-on:click="login"> login </button>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      changer: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
    login () {
      console.log('come in')
      this.$axios.post('/changer/login', {
        name: this.changer.name,
        password: this.changer.password
      })
        .then(successResponse => {
          console.log(successResponse.data)
          if (successResponse.data.code === 200) {
            console.log('ok')
          }
        })
        .catch(failResponse => {
          console.log('no ok')
        })
    }
  }
}
</script>
