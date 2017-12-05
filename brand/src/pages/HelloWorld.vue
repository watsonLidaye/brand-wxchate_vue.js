<template>
  <div class="hello">
    <div v-if="type==1">
    <loading :type="type"></loading>
    </div>
    <div v-if="type==2">
      <!-- 轮播图预留位置 -->
        <div class="banner">轮播图预留位置</div>
      <!-- 品牌介绍-->
      <!-- 小程序优势 -->
      <!-- 为什么选择天下店家 -->
      <!-- 天下店家的优势 -->
      <!-- 天下店家面对的优势 -->
      <!-- 我们的案例 -->
      <!-- tabbars -->
        <div id="tabbar" class="both">
          <a href="/" class="left">
            <div>
              <img src="../../static/image/brand/tabbar/index_checked.png" class="tab_img">
              <p class="tab_act">首页</p>
            </div>
          </a>
          <a href="/brand" class="left">
           <img src="../../static/image/brand/tabbar/brand_unchecked.png" class="tab_img">
           <p class="tab_nocat">招商</p>
         </a>
       </div>
     </div>
 </div>
</template>

<script>
import loading from '@/components/loadding'
export default {
  name: 'HelloWorld',
  components:{
    loading,
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      type:"1"
    }
  },
  beforeCreate(){
    console.log("页面加载了hello")
    setTimeout(()=>{this._data.type=2},3000)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.banner{
  width: 100%;
  height: 4rem;
  background-color: yellow;
}
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
