<template>
  <div class="pagehead">
    <a href="#" class="login-register"></a>注册登录
  </div>
</template>

<script>
export default {
  name: 'pageHead',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
<style scoped>
.pagehead{height:2.56rem;line-height: 2.56rem;text-align: left;background-color: #000;color:#fff;font-size: .64rem;}
.login-register{display: inline-block;width:.65rem;height:.65rem;border-bottom:1px solid #fff;border-left:1px solid #fff;margin-left:1rem;transform:rotate(45deg);vertical-align: middle;}
.login-lind-box a{color:#5e5e5e;margin:0 .85rem;}
.login-lind-box{text-align: center;vertical-align: text-bottom;}
.login-lind-box a.active{color:#FF2D50;font-size: 1.2rem;}
</style>
