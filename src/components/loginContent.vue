<template>
  <div class="loginContent">
    <p class="login-lind-box">
      <a href="javascript:;" :class="{'active':Active1}" @click="show(1)">登录</a>
      <a href="javascript:;" :class="{'active':Active2}" @click="show(2)">注册</a>
    </p>
  </div>
</template>

<script>
export default {
  name: 'loginContent',
  data () {
    return {
      Active1: true,
      Active2: false
    }
  },
  methods: {
    show: function (a) {
      if (a === 1) {
        this.Active1 = true
        this.Active2 = false
      } else {
        this.Active1 = false
        this.Active2 = true
      }
    }
  }
}
</script>
<style scoped>
.pagehead{height:2.56rem;line-height: 2.56rem;text-align: left;background-color: #000;color:#fff;font-size: .64rem;}
.pagehead .register{display: inline-block;width:.65rem;height:.65rem;border-bottom:1px solid #fff;border-left:1px solid #fff;margin-left:1rem;transform:rotate(45deg);vertical-align: middle;}
.login-lind-box a{color:#5e5e5e;margin:0 .85rem;font-size: .7rem;}
.login-lind-box{text-align: center;vertical-align: text-bottom;margin-top:1.5rem;}
.login-lind-box a.active{color:#FF2D50;font-size: 1.2rem;}
.login-content-box{padding:1.5rem;}
</style>
