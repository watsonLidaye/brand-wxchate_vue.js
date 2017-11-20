<template>
  <div id="app">
   
    <router-view/>
  </div>

</template>

<script>
import './js/public.js'
export default {
  name: 'app',
  computed:{
    tab_index(){
      return this.$store.state.tab_index
    }
  }
}
</script>

<style>
@import "./css/common.css";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#tabbar{
  width: 100%;
  position: fixed;
  bottom: 0rem;
  z-index: 100;
  border-top: .02rem solid #eee;
  font-size: .22rem
}
.inline_block{
  display: inline-block;
}
#tabbar>a{
  width: 50%;
  padding: .2rem 0;
}
#tabbar>.left>div{
  width: 1rem;
  margin: 0 auto;
  text-align: center;
}
.tab_img{
  width: .4rem;
  height:.4rem;
  margin-bottom: .05rem;
}
.tab_act{
  color:#ef3939;
}
.tab_nocat{
  color:#333;
}
</style>
