<template>
  <div id="register">
    <router-link to="/Login"><span class="iconfont header">&#xe606;</span></router-link>
    <p class="register-p">注册新用户</p>
    <form action="#" method="post" name="form">
      <div class="register-tel">
        <span class="iconfont">&#xe613;</span>
        <input type="text" name="tel" placeholder="请输入手机号" @blur="GetUserP"/>
      </div>
      <router-link to="/RNoteGet"><a href="" class="register-geting">获取验证码</a></router-link>
    </form>
    <p v-show="phoneAlert">请输入正确的手机号</p>
  </div>
</template>

<script>
  export default {
    name: 'Register',
    data () {
      return {

      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  #register {  display: flex;
    flex-direction:column;
    justify-content:center;
    font-family: Arial, Verdana, Tahoma, "微软雅黑", "黑体";}
  a { text-decoration: none;
    display:block;}
  .header { position:absolute;
    left:0.2rem;
    top:0.1rem;
    font-size: 0.3rem;}
  .register-p {
    width:80%;
    font-size: 0.36rem;
    font-weight: bold;
    margin:1.47rem auto 0.30rem auto;
    text-align: left;
  }
  form input {
    border:none;
    font-size: 0.22rem;
    line-height:1rem;
  }
  form div {  width:80%;
    height:1.3rem;
    line-height:1.3rem;
    font-size:0.50rem;
    border-bottom:0.01rem solid #ccc;
    margin:0 auto;
    text-align: left;
    display:flex;
    flex-direction: row;
    justify-content: space-between;
    padding-top:0.3rem;
  }
  .register-geting {  width:80%;
    height:0.9rem;
    margin:0.8rem auto;
    text-align:center;
    line-height:0.9rem;
    font-size:0.34rem;
    background-color:#f3344a;
    color:#ffffff;
    border-radius:0.05rem;}
</style>
