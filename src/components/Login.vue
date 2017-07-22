<template>
  <div class="login">
    <pageHead></pageHead>
    <loginContent @cha="changeContent"></loginContent>
    <components :is="states"></components>
    <!-- <loginContentBox></loginContentBox> -->
  </div>
</template>

<script>
import pageHead from './pageHead'
import loginContent from './loginContent'
import loginContentBox from './loginContentBox'
import registerContentBox from './registerContentBox'
export default {
  components: {
    pageHead,
    loginContent,
    loginContentBox,
    registerContentBox
  },
  name: 'pagelogin',
  data () {
    return {
      states: 'loginContentBox',
      pagelogin: 'loginContentBox'
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
