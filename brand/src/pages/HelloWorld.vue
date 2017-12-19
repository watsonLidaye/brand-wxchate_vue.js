<style scoped>
@import "../css/public.css";
.hello{
  padding-bottom: 1.3rem
}
.w_33{
  width: 33%;
  text-align: center;
}
.intro_title{
  width: 6.7rem;
  margin: 0 auto;
  font-size: 0.24rem;
  margin-bottom: 0.48rem;
}
.intrduce{
  padding-top: .64rem;
  padding-bottom: 0.92rem;
  text-align: center;

}

.title{
  font-size: 0.42rem
}
.pb40{
  padding-bottom: 0.4rem
}
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
.branner_img{
  width: 100%;
  height: 100%
}
.intro_t{
  font-size: .5rem;
  color: #ef3939;
  margin-bottom: .1rem
}
.hen_line{
  width: .2rem;
  border: 1px solid rgba(0,0,0,.2);
  margin-bottom: .16rem
}
.intro_bto{
  text-align: center;
}
.intro_text{
  font-size: .22rem;
  color: #333;
  font-weight: bold;
}
.video{
  width: 5.9rem;
  height: 3.3rem;
  background-color: #04202d;
  position: relative;
  margin-bottom: .88rem
}
.w80h80{
  width: .8rem;
  height: .8rem;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-top: -.4rem;
  margin-left: -.4rem
}
#tabbar{
  background:#fff; 
}
.nice{
  width: 100%;
  padding-top: .65rem;
  padding-bottom: .3rem;
  background: #f2f2f2;
  text-align: center;
}
.w690h190{
  width: 6.9rem;
  height: 1.9rem;
  background-color: #fff;
  border-radius: 4rpx;
  margin-bottom: .3rem
}
.w130{
  width: 1.3rem;
  position: relative;
}
.w560{
  width: 5.6rem
}
.w62h60{
  width: .62rem;
  height: .6rem;
  position: absolute;
  left: 50%;
  top: 50%;
  margin-left: -.31rem;
  margin-top:-.3rem;
}
.pt32{
  padding-top: .32rem;
}
.reason{
  width: 100%;
  padding-top: .6rem;
  padding-bottom: 1rem
}
.w330h230{
  text-align: center;
  width: 3.3rem;
  min-height: 2.3rem;
  border-radius: .1rem;
  border: 1px solid #ddd;
  margin: 0;
  margin-right: .3rem;
  margin-bottom: .3rem;
  padding:.35rem .3rem 0rem;
}
.w40h35{
  width: .4rem;
  height: .35rem
}
.good{
  border-radius: .44rem;
  background-color: #333;
  color: #fff;
  text-align: center;
  line-height: .85rem;
  margin-bottom: .3rem
}
.good1{
  background-color: #ffe0d9;
  color: #d50808
}
.good2{
  background-color: #feedbc;
  color: #ff3600
}
.good3{
  background-color: #d2f4d0;
  color: #078500
}
.good4{
  background-color: #d2e3f2;
  color: #004f95
}
</style>
<template>
  <div class="hello">
    <div v-if="type==1">
      <loading :type="type"></loading>
    </div>
    <div v-if="type==2">
      <!-- 轮播图预留位置 -->
      <div class="banner">
        <wc-swiper :duration="1000" :interval="5000" >
          <wc-slide v-for="(banner_index, key) in banner" :key="key">
            <img :src="banner_index" class="branner_img">
          </wc-slide>
      <!--     <wc-slide>
            <img src="../../static/image/brand/index/swiper1.png" class="branner_img">
          </wc-slide> -->
        </wc-swiper>
      </div>
      <!-- 品牌介绍-->
      <div class="intrduce">
        <p class="pb40">小程序品牌介绍</p>
        <p class="intro_title">
          天下店家是一款基于微信生态开发的开店软件，为实体商户提供开店管理和运营服务。微信小程序是无需下载安装即可使用的应用，微信小程序让商家坐拥9亿微信用户市场，快捷方便、业务量翻番的梦想“触手可及”。
        </p>
        <div class="intro_bto clearfix">
          <div class="left w_33">
            <p class="intro_t">1</p>
            <p class="hen_line marginA"></p>
            <p class="intro_text">每周迭代1次</p>
          </div>
          <div class="left w_33">
           <p class="intro_t">2000</p>
           <p class="hen_line marginA"></p>
           <p class="intro_text">小程序相关功能</p>
         </div>
         <div class="left w_33">
           <p class="intro_t">300</p>
           <p class="hen_line marginA "></p>
           <p class="intro_text">种培训方式</p>
         </div>
       </div>
     </div>
     <div class="video marginA">
       <img src="../../static/image/brand/brand/20.png" class="w80h80">
     </div>
     <!-- 小程序优势 -->
     <div class="nice">
       <p class="marginA ft42 color_33 font_bold mb40">小程序优势</p>
       <div v-for="(nice_item,key) in nice" class="w690h190 marginA clearfix">
         <div class="w130 left h_100">
           <img :src="nice_item.src" class="w62h60">
         </div>
         <div class="w560 left h_100 pt32 bor_border overflow">
           <div class="ft30 color_33 font_bold text_left mb25" >{{nice_item.title}}</div>
           <div class="ft22 text_left pr20">{{nice_item.content}}</div>
         </div>
       </div>
     </div>
     <!-- 为什么选择天下店家 -->
     <div class="reason">
        <p class="marginA ft42 color_33 font_bold mb40">为什么选天下店家</p>
        <ul class=" clearfix marginA bor_border ml30">
          <li class="left w330h230 bor_border" v-for="(reason_index,key) in reason" :class="{act:key==1}">
            <img :src="reason_index.src" class="w40h35 mt15">
            <p class="ft30 color_33 font_bold mt15" >{{reason_index.title}}</p>
            <p class="ft24 color_33">{{reason_index.content}}</p>
          </li>
        </ul>
     </div>
     <!-- 天下店家的优势 -->
     <div class="reason">
        <p class="marginA ft42 color_33 font_bold mb40">天下店家的优势</p>
        <ul class="  marginA bor_border ">
          <li class="w690 bor_border h85 good ft30" v-for="(good_index,key) in good" :class="{good1:key==0,good2:key==1,good3:key==2,good4:key==3,}">
           {{good_index}}
         </li>
        </ul>
     </div>
     <!-- 天下店家面对的优势 -->
     <!-- 我们的案例 -->
     <!-- tabbars -->
     <div id="tabbar" class="clearfix">
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
      type:"1",
      banner:[
        "../../static/image/brand/index/swiper1.png",
        "../../static/image/brand/index/swiper1.png",
        "../../static/image/brand/index/swiper1.png"
      ],
      nice:[
        {
          src:"../../static/image/brand/index/icon1.png",
          title:"可为企业带来大批潜在客户",
          content:"基于微信的9亿用户量，搭上微信小程序的大浪潮，一键分享，为企业拓展新客源，扩大曝光提升销售率。"
        },
        {
          src:"../../static/image/brand/index/icon2.png",
          title:"有效形成企业微信的商业闭环",
          content:"打通用户、内容信息、商品服务之间的关系，直接在微信生态体系内完成选购、下单、支付整个商业模式的闭环。"
        },
        {
          src:"../../static/image/brand/index/icon3.png",
          title:"企业营销方式更加丰富",
          content:"深化企业的营销布局，小程序和公众号相互互补，结构化、图表化的会员数据，深入了解客户，增强用户黏性，降低流失率。"
        },
      ],
      reason:[
        {
          src:"./../static/image/brand/brand/05.png",
          title:"咨询服务",
          content:'有问必答，我们关切您的问题'
        },
        {
          src:"./../static/image/brand/brand/06.png",
          title:"技术团队",
          content:'术业有专攻，实力领先同行'
        },
        {
          src:"./../static/image/brand/brand/07.png",
          title:"运营推广",
          content:'网络媒体，软文推广等广告宣传支持'
        },
        {
          src:"./../static/image/brand/brand/08.png",
          title:"技能培训",
          content:'每月召开一次加盟商分享培训大会，提供视频/PPT'
        },
        {
          src:"./../static/image/brand/brand/09.png",
          title:"物料支持",
          content:'提供产品资料，运营培训资料等一系列物料支持'
        },
        {
          src:"./../static/image/brand/brand/10.png",
          title:"售后服务",
          content:'定期更新小程序新的功能和运营玩法。'
        },
      ],
      good:[
        "版本丰富，核心功能直击刚需",
        "代理商拥有自己的后台管理系统",
        "开放开源服务",
        "用户体验好流畅体验内嵌于微信接近原生APP",
      ]
    }
  },
  beforeCreate(){
    console.log("页面加载了hello")
    setTimeout(()=>{this._data.type=2},3000)
  },
  method:{

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

