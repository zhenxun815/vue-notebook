<!-- List -->
<template>
  <div>
    <ul>
      <li v-for="(item,index) in pageLists"
          :key="index">
        {{item.title}}-{{item.content}}</li>
    </ul>
  </div>
</template>

<script>
import store from '../store.js'
export default {
  name: 'List',
  store,
  data () {
    return {
    }
  },
  components: {},
  computed: {
    pageLists () {
      return store.state.lists
    }
  },
  methods: {}
}

</script>
<style scoped>
</style>
