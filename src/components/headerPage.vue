<template>
  <div class="headerPage">
   <img src="../../static/img/logo.png" alt="" class="logo">
   <router-link to="Login" class="user"></router-link>
  </div>
</template>
<script>
export default {
  components: {
  },
  name: 'headerPage',
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.headerPage{height:2.56rem;text-align: left;background-color: #07111b;}
.logo{height:2rem;margin-top:.28rem;margin-left:.64rem;}
.user{float:right;height:1.5rem;width:1.5rem;background: url(../../static/img/user.jpg) no-repeat center;background-size:100% 100%;margin-top:.53rem;margin-right:.64rem;}
</style>
