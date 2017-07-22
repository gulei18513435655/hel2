<template>
<div>
  <div class="login-content-box">
    <ul>
      <li>
        <input type="text" v-model="phoneInput" class="input-phone" placeholder="手机号或邮箱" @blur="phoneVerification">
        <p v-show="phoneBoolean" class="error-text">请输入正确的邮箱或手机号</p>
      </li>
      <li>
        <input class="input-phone" placeholder="请输入密码" @blur="passwordVerification" v-model="phonePassword">
        <p v-show="passwordBoolean" class="error-text imwap-visibility js-showpw">请输入6-16位密码，区分大小写，不能使用空格！</p>
        <a href="javascript:;" class="eyes-img" @click="changeType"></a>
      </li>
    </ul>
    <router-link to="firstPage" class="login-btn">登录</router-link>
    <a href="#" class="forgot">忘记密码</a>
    
  </div>
  <div class="account-sns-login">
    <p class="other-login">其他方式登录</p>
    <p class="other">
      <a href="#"><img src="../../static/img/qq.jpg" alt=""></a>
      <a href="#"><img src="../../static/img/weibo.jpg" alt=""></a>
    </p>
  </div>
</div>
</template>

<script>
export default {
  name: 'loginContentBox',
  data () {
    return {
      inputType: 'password',
      phoneInput: '',
      phonePassword: '',
      phoneBoolean: false,
      passwordBoolean: false
    }
  },
  methods: {
    phoneVerification: function () {
      if ((/^([a-zA-Z0-9_-])+@([a-zA-Z0-9_-])+(.[a-zA-Z0-9_-])+/).test(this.phoneInput) || (/^1(3|4|5|7|8)\d{9}$/).test(this.phoneInput)) {
        this.phoneBoolean = false
      } else {
        this.phoneBoolean = true
      }
    },
    passwordVerification: function () {
      if ((/^(\w){6,18}$/).test(this.phonePassword) && this.phonePassword !== '') {
        this.passwordBoolean = false
      } else {
        this.passwordBoolean = true
      }
    },
    changeType: function () {
      if (this.inputType === 'password') {
        this.inputType = 'text'
      } else {
        this.inputType = 'password'
      }
    }
  }
}
</script>

<style scoped>
.login-content-box{padding:0 1.7rem;}
.login-content-box ul{margin-top:2rem;}
.login-content-box ul li{padding-bottom:.4rem;position: relative;}
.input-phone{width:100%;height:2.24rem;font-size: 0.8rem;border: 1px solid #d9dde1;padding:0 .64rem;box-sizing: border-box;color: #787d82;line-height:2.24rem;margin-bottom:.4rem;border-radius:0.26rem;}
.error-text{color:#ff2d50;font-size: .6rem;text-align: left;padding-left:.64rem;line-height: 1rem;}
.login-btn{display: block;color: #fff;background: #ff2d50;font-size: .83rem;line-height: 2.56rem;border-radius: .26rem;}
.forgot{font-size: .75rem;color:#5e5e5e;}
.account-sns-login{position: absolute;width:100%;bottom: 0;text-align: center;margin-bottom: .8rem;}
.other-login{font-size: .75rem;}
.other{text-align:center;margin-top:0.812rem;}
.other a{margin:0 .5rem;}
/*.input-eyes{background: url("../../static/img/eyes.jpg") no-repeat 90% center;background-size:1.25rem .8rem;}*/
.eyes-img{position: absolute;height:2.24rem;width:1.25rem;left:90%;top:0;background: url("../../static/img/eyes.jpg") no-repeat 90% center;background-size:100% .8rem;}
</style>
