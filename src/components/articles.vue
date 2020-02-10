<template>
    <div class="main">
        <div class="content" v-for="item in items" :key="item.index">
            <a href="#"><img :src="item.picUrl"></a>
            <span><a href="#"><h3>{{item.dataA}}</h3></a><p>{{item.timeA}}</p></span>
            <span><a href="#"><h3>{{item.dataB}}</h3></a><p>{{item.timeB}}</p></span>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          picUrl: require('../assets/news_bg_1.png'),
          dataA: '江苏密斯欧与公牛集团宣布达成战略合作',
          timeA: '2019/07/30',
          dataB: '江苏密斯欧与美的联合会战略合作启动',
          timeB: '2019/01/31'
        },
        {
          picUrl: require('../assets/news_bg_2.png'),
          dataA: '苏州密斯欧举办首届青少年科学小会 发布弱电工程项目科学看点榜单',
          timeA: '2019/07/30',
          dataB: '苏州发布弱电工程项目，密斯欧为全球首家获奖企业',
          timeB: '2019/01/31'
        },
        {
          picUrl: require('../assets/news_bg_3.png'),
          dataA: '河南密斯欧布局产业互联网 迎接全球数字化发展机遇',
          timeA: '2019/07/30',
          dataB: '河南首届中国智慧媒体的大会在通许召开，密斯欧发布4款智慧出行方案',
          timeB: '2019/01/31'
        }
      ]
    }
  }
}
</script>

<style scoped>
    .main{
        position: relative;
        height: 500px;
        overflow: hidden;
        min-width: 1300px;
        background:  #f5f8fa;
        margin-bottom: 150px;
    }
    .main .content{
        margin-left: 2rem;
        height: 400px;
        float: left;
        width: 30%;
    }
    .main .content h3{
      font-weight: normal;
      margin-top: 50px;
    }
    .main .content p{
      opacity: 0.5;
      margin-top: 10px;
    }
    .main .content a{
        text-decoration: none;
        color: black;
    }
    .main .content img{
        width: 100%;
        height: 200px;
    }
    .main .content span{
        margin-top: 2rem;
        font-size: 20px;
    }
</style>
