<template>
  <div class="loginbody">
    <div class="logindata">
      <div class="logo">
        <img src="../assets/logo.png" alt="">
      </div>
      <div class="loginway">
        <button class="waybutt" id="butt1" @click="toform1">账户密码登录</button>
        <button class="waybutt" id="butt2" @click="toform2">手机号登录</button>
      </div>
      <div class="formdata">
        <div id="formdiv1">
          <form class="login-form" id="form1" action="loginWithAccount" >
            <div class="formline">
              <span class="el-icon-s-custom"></span>
              <input type="text" placeholder="账户" v-model="account">
            </div>
            <div class="formline">
              <span class="el-icon-s-lock"></span>
              <input type="password" placeholder="密码" v-model="passWord">
            </div>
          </form>
        </div>
        <div id="formdiv2" style="display:none">
          <form class="login-form" id="form2" action="loginWithCode">
            <div class="formline">
              <span class="el-icon-s-custom"></span>
              <input type="text" placeholder="手机号" v-model="account">
            </div>
            <div class="formline">
              <span class="el-icon-s-lock"></span>
              <div class="special-formline">
                <input type="password" placeholder="验证码" v-model="passWord">
                <button>获取验证码</button>
              </div>
            </div>
          </form>
        </div>
      </div>
      <div class="tool">
        <div>
          <span class="fgtpasswd" @click="forgetpasswd" style="color:rgb(24, 144, 255);">忘记密码</span>
        </div>
      </div>
      <div class="butt">
        <button type="primary" @click="login()">登 录</button>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'login',
  data() {
    return {
      form: {
        account: '123123',
        passWord: '123123',
      },
      rules: {
        account: [{ required: true, message: '请输入账号', trigger: 'blur' }],
        passWord: [{ required: true, message: '请输入密码', trigger: 'blur' }],
      },
    };
  },
  methods: {

    login(form){
      this.$router.push('/main')
    },
    toform1(){
      document.getElementById("formdiv2").style.display="none"
      document.getElementById("formdiv1").style.display=""
    },
    toform2(){
      document.getElementById("formdiv2").style.display=""
      document.getElementById("formdiv1").style.display="none"
    }
  },
};
</script>

<style scoped>
.loginbody {
  width: 100%;
  height: 100%;
  position: relative;
}

.logindata {
  vertical-align: middle;
  margin: auto;
  width: 300px;
  height: 600px;

}

.logo{
  margin-top: 100px;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.loginway {
  margin-top: 10px;
  text-align: center;
  width: 100%;
}

.loginway button{
  background-color: transparent;
  font-size: 16px;
  border: none;
  color: grey;
  padding: 8px;
  margin: 10px;
  width: 120px;
}

.loginway button:focus{
  border-bottom: solid 2px rgb(24, 144, 255);
  color: rgb(24, 144, 255);
}

.tool {
  padding-top: 10px;
  padding-bottom: 10px;
  margin-right: -10px;
  text-align: right;
}

.butt {
  margin-top: 10px;
  text-align: center;
  width: 100%;
}

.butt button{
  background-color: rgb(24, 144, 255);
  border-radius: 4px;
  font-size: 16px;
  border: none;
  color: #fff;
  padding: 8px;
  margin-left: 10px;
  width: 100%;
}

.login-form{
  width: 100%;
  margin: 0%;
}

.formline {
  position: relative;
  padding: 10px;
  width: 100%;
}

.formline input{
  border-width: 1px;
  border-color: rgba(0, 0, 0, 0.2);
  padding: 8px;
  width: 280px;
}

.special-formline{
  display: inline-block;
  justify-content: left;
  width:100%;

}

.special-formline input{
  border-width: 1px;
  border-color: rgba(0, 0, 0, 0.2);
  padding: 8px;
  
  width: 170px;
}
.special-formline button{
  border-width: 1px;
  border-color: rgba(0, 0, 0, 0.2);
  padding: 6px;
  margin-left: 10px;
  width: 100px;
}

</style>