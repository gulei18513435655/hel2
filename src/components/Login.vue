<template>
  <div class="login">
    <pageHead></pageHead>
    <loginContent></loginContent>
    <loginContentBox></loginContentBox>
  </div>
</template>

<script>
import pageHead from './pageHead'
import loginContent from './loginContent'
import loginContentBox from './loginContentBox'
export default {
  components: {
    pageHead,
    loginContent,
    loginContentBox
  },
  name: 'pagelogin',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
