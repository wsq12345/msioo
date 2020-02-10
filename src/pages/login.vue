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
        >登录</el-button>
        <el-button
          type="success"
          @click="register()"
        >注册</el-button>
      </el-form>
    </div>
    <div class="form-container" v-if="!show">
      <h2>用户注册</h2>
      <el-form label-position="top" :model="formData" :rules="rules" ref="formData">
        <el-form-item label="用户名" prop="username2">
          <el-input v-model="formData.username2"></el-input>
        </el-form-item>
        <el-form-item label="密码" prop="password2">
          <el-input v-model="formData.password2" type="password"></el-input>
        </el-form-item>
        <el-form-item label="再输一遍密码" prop="password3">
          <el-input v-model="formData.password3" type="password"></el-input>
        </el-form-item>
        <el-button
          type="success"
          @click="back()"
        >返回</el-button>
        <el-button
          type="success"
          @click="submitRegister('formData')"
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
        password: '',
        username2: '',
        password2: '',
        password3: ''
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
        ],
        username2: [
          { required: true, message: '请输入用户名', trigger: 'blur' },
          {
            min: 3,
            max: 10,
            message: '用户名长度需在3-10个字符之间',
            trigger: 'blur'
          }
        ],
        password2: [
          { required: true, message: '请输入密码', trigger: 'blur' },
          { min: 6, message: '密码长度至少6个字符', trigger: 'blur' }
        ],
        password3: [
          { required: true, message: '请输入密码', trigger: 'blur' },
          { min: 6, message: '密码长度至少6个字符', trigger: 'blur' }
        ]
      }
    }
  },
  methods: {
    register () {
      this.show = false
    },
    submitForm (data) {
      let users = JSON.parse(sessionStorage.getItem('user'))
      if (this.formData.username === users.username && this.formData.password === users.password) {
        alert('登录成功')
      }
    },
    submitRegister (data) {
      if (this.formData.password2 !== this.formData.password3) {
        alert('2次输入不一样')
      } else {
        let users = JSON.stringify({username: this.formData.username2, password: this.formData.password2})
        sessionStorage.setItem('user', users)
        alert('注册成功,请返回登录')
      }
    },
    back () {
      this.show = true
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
