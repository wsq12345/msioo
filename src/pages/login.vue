<template>
  <div id="login">
    <div class="form-container" v-if="show">
      <h2>用户登录</h2>
      <el-form label-position="top" :model="formData" :rules="rules" ref="formData">
        <el-form-item label="用户名" prop="username">
          <el-input v-model="formData.username"></el-input>
        </el-form-item>
        <el-form-item label="密码" prop="password">
          <el-input v-model="formData.password" type="password"></el-input>
        </el-form-item>
        <el-button
          type="success"
          @click="submitForm('formData')"
          :loading="logining"
        >登录</el-button>
        <el-button
          type="success"
          @click="register()"
          :loading="logining"
        >注册</el-button>
      </el-form>
    </div>
    <div class="form-container" v-if="!show">
      <h2>用户注册</h2>
      <el-form label-position="top" :model="registerData" :rules="rules" ref="formData">
        <el-form-item label="用户名" prop="username">
          <el-input v-model="formData.username"></el-input>
        </el-form-item>
        <el-form-item label="密码" prop="password">
          <el-input v-model="formData.password" type="password"></el-input>
        </el-form-item>
        <el-form-item label="再输一遍密码" prop="password">
          <el-input v-model="formData.passworda" type="password"></el-input>
        </el-form-item>
        <el-button
          type="success"
          @click="submitRegister('formData')"
          :loading="logining"
        >确认注册</el-button>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      logining: false,
      show: true,
      formData: {
        username: '',
        password: ''
      },
      registerdata: {
        username: '',
        password: '',
        passworda: ''
      },
      rules: {
        username: [
          { required: true, message: '请输入用户名', trigger: 'blur' },
          {
            min: 3,
            max: 10,
            message: '用户名长度需在3-10个字符之间',
            trigger: 'blur'
          }
        ],
        password: [
          { required: true, message: '请输入密码', trigger: 'blur' },
          { min: 6, message: '密码长度至少6个字符', trigger: 'blur' }
        ]
      }
    }
  },
  methods: {
    register () {
      this.show = false
    }
  }
}
</script>

<style scoped>
#login {
  height: 100%;
  background: url(../assets/bg1.jpg) no-repeat;
  background-size: 100% 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
#login .form-container {
    background: #1f2d3d;
    width: 500px;
    text-align: center;
    padding: 40px;
    border-radius: 20px;
    box-sizing: border-box;
}
</style>
