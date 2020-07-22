<template>
  <div class="login_container">
    <div class="login_box">
      <!-- 头像区域-->
      <div class="avatar_box">
        <img src="../assets/logo.png" alt="你的图挂了">
      </div>
      <!-- 登录表单区域-->
      <el-form ref="loginFormRef" :model="loginForm" label-width="0px" class="login_form">
        <!-- 用户名区域-->
        <el-form-item prop="username">
          <el-input v-model="loginForm.username" prefix-icon="iconfont icon-user"></el-input>
        </el-form-item>
        <!--密码区域-->
        <el-form-item prop="password">
          <el-input v-model="loginForm.password" prefix-icon="iconfont icon-3702mima" type="password"></el-input>
        </el-form-item>
        <!--按钮区域-->
        <el-form-item class="buttons">
          <el-button type="primary">登录</el-button>
          <el-button type="info">注册</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      // 这是登录表单的数据绑定对象
      loginForm: {
        // 后面引号可以设置默认值
        username: 'admin',
        password: '123456'
      }
    }
  }
}
</script>

<style lang="less" scoped>
  .login_container{
    background: linear-gradient(to right bottom,lightseagreen,orangered);
    height:100%;
  }
  .login_box{
    width:450px;
    height:300px;
    background-color: wheat;
    border-radius: 3px;//圆角边框
    position: absolute;//绝对定位
    left: 50%;
    top:30%;
  }

  .login_box{
    transform: translate(-50%);
  }
  .avatar_box{
    height:130px;
    width:130px;
    border:1px solid lightcoral;
    background-color: wheat;
    border-radius:50%;//边框设置为圆角
    padding: 10px;//内边距
    box-shadow: 0 0 10px orangered;//加阴影
    /*头像往右移动到中间*/
    position: absolute;//绝对定位
    left: 50%;//往右边移动50%
    //再往左移动头像自身的50%,第二个参数是往上移动50%
    transform: translate(-50%,-50%);

    img{
      width:100%;
      height:100%;
      border-radius: 50%;//图片设置为圆形
      background-color: tomato;
    }
  }
  .buttons{
    display: flex;//弹性盒子
    justify-content: flex-end;
  }
  .login_form{
    position: absolute;
    bottom: 0;
    width:100%;
    padding: 0 20px;
    box-sizing:border-box;
  }
</style>
