<template>
    <div class="my">
        <div class="myHeader">{{my}}</div>
        <div class="myMain">
            <div class="Main">
                <img src="/static/img/2018-03-12_132733.png" alt="头像">
                <p>{{myName}}</p>
            </div>
        </div>
        <div class="MyBox">
            <div class="myOrder" @click="order">
                <div class="Order">
                    <i class="iconfont icon-74wodedingdan"></i>
                    <p>我的订单</p>
                </div>
            </div>

            <div class="myCollection" @click="author">
                <div class="Order">
                    <i class="iconfont icon-zuozhe"></i>
                    <p>看到这个项目的小伙伴，麻烦点一下这里~</p>
                </div>
            </div>
        </div>
       
    </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name:"my",
  data(){
      return{
        my:"关于我",
        myName:"Xiao Hai"
      }
  },
  methods:{
      order:function(){
         this.$router.push('/order')
      },
      author:function(){
          this.$router.push('/author')
      }
  }
}
</script>


<style>
   .myHeader{
        height: 1.3rem;
        line-height: 1.3rem;
        font-size: 0.35rem;
        padding-left: 0.3rem;
        background: white;
        font-size: 0.41rem;
   }
   
   .myMain{
       height: 100%;
       background: white;
       margin-top: 10px;
       width: 100%;
       
   }
    .MyBox{
        width: 100%;
        height: 110px;
        background: white;
    }
    .myOrder,.myCollection{
        height: 50%;
    }
   .Main, .Order{
       height: 100%;
       /* background: red; */
       margin-left: 10px;
       border-bottom: 1px solid #cccccc;
   }
   .myMain img{
       display: block;
       width: 60px;
       height: 60px;
       padding: 7px;
       float: left;
   }
    .myMain p{
        line-height: 75px;
    }
  
   .Order i , .Order p{
       display: block;
       line-height: 55px;
       float: left;
       padding-left: 10px;
   }
</style>
