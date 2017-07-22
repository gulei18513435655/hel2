
<template>
  <div class="firstPage">
   <headerPage></headerPage> 
  </div>
</template>

<script>
import headerPage from './headerPage'
export default {
  components: {
    headerPage
  },
  name: 'firstPage',
  data () {
    return {
    }
  },
  methods: {
    changeContent: function (componentsName) {
      this.states = componentsName
      console.log(this.states)
    }
  }
}
</script>

<style scoped>

</style>
