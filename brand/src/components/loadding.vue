<template>
  <div class="loading">
    <div v-if="type==1">1</div>
    <div v-if="type==2">2</div>
  </div>

</template>

<script>

export default {
  name: 'loading',
  props:['type'],
  data () {
    return {
      // type:1, //加载的状态，1为加载中，2为加载成功，3为加载失败，4为下拉加载
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
