<template>
    <div class="home">
        <headerGuide></headerGuide>
        <div class="zanwei"></div>
        <slider></slider>
        <div class="about-wrap">
            <h1 class="title">重塑新匠人精神 &nbsp;创造新服务场景</h1>
            <p>Msioo密斯欧，2012年成立于苏州，以互联网为基础的科技服务型公司。</p>
            <p>努力发展成为优秀的服务平台，做到商家放心、师傅开心、员工幸福。</p>
            <p>诚信、敬业、积极、创新、合作、担当</p>
            <a href="#" class="more">了解更多</a><i class="iconfont icon-iconfontjiantou5"></i>
        </div>
        <articles></articles>
        <footerGuide></footerGuide>
    </div>
</template>

<script>
import headerGuide from '../components/headerGuide'
import slider from '../components/slider'
import articles from '../components/articles'
import footerGuide from '../components/footerGuide'
export default {
  data () {
    return {
    }
  },
  methods: {
    suofang () {
      var num = 1300// css中固定的网页宽度
      var oWidth = window.screen.width// 获取当前手机屏幕宽度
      var rate = oWidth / num// 缩放比例 = 当前手机屏幕宽度/css中固定的网页宽度
      if (oWidth < 1920) {
        // eslint-disable-next-line no-global-assign
        document.getElementsByTagName('meta')[name = 'viewport'].content = 'width=device-width,height=device-height,initial-scale=1.0,maximum-scale=1.0,user-scalable=no,width=device-width,height=device-height,initial-scale=' +
        rate + ',maximum-scale=2.0,user-scalable=no'// 修改meta的属性
      }
    }
  },
  mounted () {
    this.suofang()
  },
  components: {
    headerGuide,
    slider,
    articles,
    footerGuide
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .home{
        min-width: 1300px;
    }
    .zanwei{
        width: 100%;
        height: 70px;
    }
    .about-wrap{
        text-align: center;
        margin: 150px 0 150px 0;
    }
    .about-wrap p{
        margin-bottom: 10px;
        font-size: 20px;
    }
    .about-wrap a{
        text-decoration: none;
        color: black;
        margin-top: 20px;
    }
    .about-wrap .iconfont{
        color: red;
    }
</style>
