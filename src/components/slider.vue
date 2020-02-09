<template>
  <el-carousel height="30rem" indicator-position="outside">
    <el-carousel-item v-for="pic in pics" :key="pic.index">
      <img :src="pic" />
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  data () {
    return {
      pics: [
        require('../assets/b1.jpg'),
        require('../assets/b2.jpg'),
        require('../assets/b3.jpg'),
        require('../assets/b4.jpg')
      ]
    }
  }
}
</script>

<style>
.el-carousel {
  margin-left: 50%;
  transform: translateX(-50%);
  min-width: 1300px;
}
img {
  width: 100%;
  height: 100%;
}
.el-carousel__button {
  width: 1rem;
}
</style>
