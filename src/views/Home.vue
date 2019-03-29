<!-- Home -->
<template>
  <div>
    <router-view />
    <ul>
      <li>
        <router-link :to="{name: 'list'}">笔记列表</router-link>
      </li>
      <li>
        <router-link :to="{name: 'user'}">个人中心</router-link>
      </li>
    </ul>
  </div>

</template>

<script>
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
<style scoped>
</style>
