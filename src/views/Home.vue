<!-- Home -->
<template>
  <div>
    <router-view />
    <ul class="footer">
      <li class="tabs">
        <router-link :to="{name: 'list'}">笔记列表</router-link>
      </li>
      <li class="tabs">
        <router-link :to="{name: 'user'}">个人中心</router-link>
      </li>
    </ul>
  </div>

</template>

<script>
import '../assets/stylus/home.styl'

export default {
  name: 'Home',
  data () {
    return {
    }
  },
  components: {},
  computed: {},
  methods: {}
}

</script>
<style scoped lang="stylus" >
</style>
