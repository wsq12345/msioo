<template>
    <footer class="foot">
        <div class="footer_attention" v-for="title in titles" :key="title.index">
        <h2 class="title">{{title.name}}</h2>
        <ul class="link_list">
            <li v-for="detail in title.details" :key="detail.index">
                <a href="#" target="_blank">{{detail}}</a>
            </li>
        </ul>
        </div>
        <div class="footer_icon">
            <h1 class="logo">密斯欧</h1>
            <a href="#"><img src="../assets/pic.gif"></a>
            <h5>Copyright © 2005 - 2019 Msioo. All Rights Reserved.密斯欧 版权所有</h5>
            <a href="#" target="_blank">苏ICP备16035725号-5</a>
            增值电信业务经营许可证：
            <a href="#" target="_blank">苏B2-20170504</a>
            苏公网安备:32058302001036号<br />
        </div>
    </footer>
</template>

<script>
export default {
  data () {
    return {
      titles: [
        {name: '业务体系', details: ['锁安帮', '弱电工程', '通许视窗']},
        {name: '联系我们', details: ['江苏密斯欧', '苏州密斯欧', '河南密斯欧', '永康密斯欧']},
        {name: '加入我们', details: ['关于我们', '公司动态', '社会招聘']}
      ]
    }
  }
}
</script>

<style scoped>
    .foot{
        min-width: 1300px;
        height: 300px;
        background: #131212;
    }
    .foot div{
        float: left;
        margin-right: 4rem;
        margin-top: 2rem;
    }
    .foot ul{
        list-style: none;
    }
    .foot .title{
        color: white;
        margin-bottom: 1rem;
    }
    .foot ul a{
        text-decoration: none;
        color: white;
        opacity: 0.4;
        margin-bottom: 0.5rem;
    }
    .footer_icon{
        color: white;
    }
    .footer_icon .logo{
        height: 27px;
        width: 203px;
        background: url('../assets/logo.png') no-repeat;
        text-indent: -9999px;
    }
    .footer_icon img{
        width: 50px;
        height: 12px;
        position: relative;
        margin-top: 1rem;
        left: 150px;
    }
    .footer_icon a{
        text-decoration: none;
        color: white;
        opacity: 0.4;
    }
</style>
