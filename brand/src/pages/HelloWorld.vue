<template>
  <div class="hello">
    <div v-if="type==1">
    <loading :type="type"></loading>
    </div>
    <div v-if="type==2">
      <h1>{{ msg }}</h1>
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
      type:"2"
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
