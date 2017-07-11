<template>
  <div class="login">
    <pageHead></pageHead>
    <loginContent :logo="states"></loginContent>
    <components :is="pagelogin"></components>
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
      // pageregister: 'registerContentBox'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
