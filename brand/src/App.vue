<template>
  <div id="app">
    <!-- tabbars -->
    <div id="tabbar" class="both">
      <a href="/" class="left">
        <div>
          <img src="../static/image/brand/tabbar/index_checked.png" class="tab_img">
          <p class="tab_act">首页</p>
        </div>
      </a>
      <a href="#/brand" class="left">
       <img src="../static/image/brand/tabbar/brand_unchecked.png" class="tab_img">
          <p>招商</p>
      </a>
    </div>
    <router-view/>
  </div>

</template>

<script>
import './js/public.js'
export default {
  name: 'app'
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
</style>
