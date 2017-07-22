<template>
  <div class="login-content-box">
    <ul>
      <li>
        <input type="text" v-model="phoneInput" class="input-phone" placeholder="手机号" @blur="phoneVerification">
        <p v-show="phoneBoolean" class="error-text">手机号格式错误</p>
      </li>
      <li>
        <input type="text" v-model="phonePassword" class="input-phone input-phone-code" placeholder="请输入验证码" @blur="passwordVerification">
        <span class="code-box">
          <img src="../../static/img/code-img.jpg" alt="" class="code-img">
        </span>

        <p v-show="passwordBoolean" class="error-text imwap-visibility js-showpw">请输入正确的验证码</p>
      </li>
    </ul>
    <a href="#" class="login-btn">注册</a>
  </div>
</template>

<script>
export default {
  name: 'loginContentBox',
  data () {
    return {
      phoneInput: '',
      phonePassword: '',
      phoneBoolean: false,
      passwordBoolean: false
    }
  },
  methods: {
    phoneVerification: function () {
      if ((/^1(3|4|5|7|8)\d{9}$/).test(this.phoneInput)) {
        this.phoneBoolean = false
      } else {
        this.phoneBoolean = true
      }
    },
    passwordVerification: function () {
      if ((/[a-zA-Z0-9]{6}/).test(this.phonePassword) && this.phonePassword !== '') {
        this.passwordBoolean = false
      } else {
        this.passwordBoolean = true
      }
    }
  }
}
</script>

<style scoped>
.login-content-box{padding:0 1.7rem;}
.login-content-box ul{margin-top:2rem;}
.login-content-box ul li{padding-bottom:.4rem;text-align: left;}
.input-phone{width:100%;height:2.24rem;font-size: 0.8rem;border: 1px solid #d9dde1;padding:0 .64rem;box-sizing: border-box;color: #787d82;line-height:2.24rem;margin-bottom:.4rem;border-radius:0.26rem;}
.input-phone-code{width:70%;}
.error-text{color:#ff2d50;font-size: .6rem;text-align: left;padding-left:.64rem;line-height: 1rem;}
.code-box{float:right;width:25%;height:2.24rem;overflow:hidden;}
.code-img{width:100%;line-height: 2.24rem;height:100%;}
.login-btn{display: block;color: #fff;background: #ff2d50;font-size: .83rem;line-height: 2.56rem;border-radius: .26rem;}
</style>
