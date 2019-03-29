<!-- Login -->
<template>
  <div>
    <div v-if="!isReg">
      用户名：
      <input type="text"
             v-model="name">
      密码：
      <input type="password"
             v-model="password">
      <button @click="login">登陆</button>
      <button @click="reg">注册</button>
    </div>

    <div v-else>
      用户名：
      <input type="text"
             v-model="name">
      密码：
      <input type="password"
             v-model="password">
      确认密码：
      <input type="password"
             v-model="repeat">
      <button @click="addUser">确定</button>
      <button @click="cancel">取消</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      isReg: false,
      name: '',
      password: '',
      repeat: ''
    }
  },
  components: {},
  computed: {},
  methods: {
    login () {
      if (localStorage.getItem('name') === this.name && localStorage.getItem('password') === this.password) {
        this.$router.push('/home/list')
      } else {
        alert('用户名或密码错误！')
      }
    },
    reg () {
      this.isReg = true
    },
    addUser () {
      if (this.password === this.repeat) {
        localStorage.setItem('name', this.name)
        localStorage.setItem('password', this.password)
        this.name = ''
        this.password = ''
        this.isReg = false
      } else {
        alert('两次密码不一致！')
      }
    },
    cancel () {
      this.isReg = false
    }
  }
}

</script>
<style scoped>
</style>
