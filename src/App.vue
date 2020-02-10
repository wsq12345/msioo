<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {

    }
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
  body{
    width: 100%;
    height: 100%;
  }
  #app{
    height: 100vh;
  }
</style>
