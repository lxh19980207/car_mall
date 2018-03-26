<template>
  <div id="app">
    <router-view></router-view>
    <Footer/>
  </div>
</template>

<script>
import Rem from './rem/rem.js'
import Footer from './components/footer'
export default {
  name: 'app',
  components:{
    Footer,
  }
}
</script>

<style>
 /* @import  "//at.alicdn.com/t/font_337147_rz7i21pv98fzjjor.css"; */
 @import "./font/font.css";
body{
  padding-bottom:1.56rem; 
  font-family: '微软雅黑';
  background: #F4F4F4;;
}
</style>
