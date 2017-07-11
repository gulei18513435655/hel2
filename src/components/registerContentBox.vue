<template>
  <div class="login-content-box">
    <ul>
      <li>
        <input type="text" class="input-phone" placeholder="手机号">
        <p class="error-text">手机号格式错误</p>
      </li>
      <li>
        <input type="text" class="input-phone" placeholder="请输入验证码">
        <p class="error-text imwap-visibility js-showpw">请输入正确的验证码</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'loginContentBox',
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.login-content-box{padding:0 1.7rem;}
.login-content-box ul{margin-top:2rem;}
.login-content-box ul li{padding-bottom:.4rem;}
.input-phone{width:100%;height:2.24rem;font-size: 0.8rem;border: 1px solid #d9dde1;padding:0 .64rem;box-sizing: border-box;color: #787d82;line-height:2.24rem;margin-bottom:.4rem;}
.error-text{color:#ff2d50;font-size: .6rem;text-align: left;padding-left:.64rem;line-height: 1rem;}
</style>
