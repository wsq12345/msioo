<template>
  <header class="head">
    <div class="head_con">
      <a href="#">
        <h1 class="logo">密斯欧</h1>
      </a>
      <ul class="menu_list">
        <li>
          <a href="#">
            公司信息
          </a>
        </li>
        <li>
          <a href="#">
            企业文化
          </a>
        </li>
        <li>
          <a href="#">
            业务体系
          </a>
        </li>
        <li>
          <a href="#">
            联系我们
          </a>
        </li>
        <li class="tool">
          <a href="#" class="email" target="_blank">邮箱</a>
          <a href="#/login" class="oa" target="_blank">OA</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .head{
    background: #fff;
    min-width: 1300px;
    height: 70px;
    position: fixed;
    left: 0;
    z-index: 9999;
    border-bottom: 1px solid #f1f1f1;
    overflow: hidden;
  }
  .head_con {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
  }
  .head_con .logo {
        height: 27px;
        width: 203px;
        background: url('../assets/logo.png') no-repeat;
        text-indent: -9999px;
        overflow: hidden;
        position: absolute;
        left: 15px;
        top: 20px;
    }
  .menu_list, .menu_list li, .menu_list li a {
    width: auto;
    display: block;
  }

  .menu_list {
    height: 70px;
    position: absolute;
    right: 0;
    top: 0;
  }
  .menu_list li{
    float: left;
  }
  .menu_list li a {
    position: relative;
    float: left;
    height: 70px;
    padding: 0 30px;
    line-height: 70px;
    color: #333;
    text-decoration: none;
    font-weight: 500;
    text-align: center;
  }
  .menu_list li a:hover{
    color: red;
  }
  .menu_list .tool .email {
    color: #fff;
    background: #313131;
    height: 50px;
    line-height: 50px;
    margin-top: 10px;
}
.menu_list .tool .oa {
  background: red;
  color: white;
  height: 50px;
  line-height: 50px;
  margin-top: 10px;
}
</style>
