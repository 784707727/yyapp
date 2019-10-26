<template>
        <div id="xbb">
           <div class="a1">
             <p>我的服务</p>
           </div>
           <div class="a2">
             <div class="a3">
                 <img :src="a" alt="">
                 <span>专家问诊</span>
             </div>
             <div class="a3">
                 <img :src="b" alt="">
                 <span>专家问诊</span>
             </div>
             <div class="a3">
                 <img :src="c" alt="">
                 <span>专家问诊</span>
             </div>
           </div>
           <div class="b1">
               <p>常用工具</p>
               <div class="b3">
                   <div class='b2'>
                       <img :src='d' alt="">
                       <p>家庭档案</p>
                   </div>
                   <div class='b2'>
                        <img :src='e' alt="">
                        <p>我的处方</p>
                   </div>
                   <div class='b2'>
                    <img :src='f' alt="">
                    <p>我的医生</p>
                   </div>
                   <div class='b2'>
                    <img :src='g' alt="">
                    <p>意见反馈</p>
                   </div>
                   <div class='b2'>
                    <img :src='h' alt="">
                    <p>常见问题</p>
                   </div>
                   <div class='b2'>
                    <img :src='i' alt="">
                    <p>推荐有礼</p>
                   </div>
                   <div class='b2'>
                    <img :src='j' alt="">
                    <p>联系客服</p>
                   </div>
                   <div class='b2'>
                     <img :src='k' alt="">
                     <p @click="login">登录</p>
                   </div>
              </div>
           </div>
          
         </div> 
</template>
<script>
    export default{
        data(){
            return{

            }
        },
      props:{
       a:{default:''},
       b:{default:''},
       c:{default:''},
       d:{default:''},
       e:{default:''},
       f:{default:''},
       g:{default:''},
       h:{default:''},
       i:{default:''},
       j:{default:''},
       k:{default:''}
      },
      methods:{
          login(){
              this.$router.push("/login")
          }
      }
    }
</script>
<style scoped>
      #xbb{
          width:100%;height:500px;
          background:linear-gradient(to right,#ffffff 0%, #e6e3e6 30%,#e6e3e6 50%,#e6e3e6 75%,#ffffff 100%);
           overflow:hidden;
      }
      .a1{
          width: 315px;height: 141px;
          background: #ffffff;
          position: relative;
          top:90px;left:30px;
          border-radius: 12px;
      }
      .a1>p:nth-child(1){
          position:absolute;
          left: 50%;top: 50%;
          margin-top:-60px;margin-left: -30px;
          font-size: 14px;
          font-family: '思源黑体 Bold', '思源黑体';
          font-weight: 700;
          font-style: normal;
      }
      .a2{
          margin-top:0px;
          display: flex;
          justify-content:space-around;
      }
      .a3{
          z-index: 1;
          width: 60px;height: 60px;
      }
      .a3>span:nth-child(2){
          font-size: 12px;
      }
      .b1{
          position: relative;
          width: 315px;height: 200px;
          background: #ffffff;
          top:45px;left:30px;
            margin-bottom:60px;
      }
       .b1>p:first-child{
        position:absolute;
          left: 50%;top: 50%;
          margin-top:-85px;margin-left: -30px;
          font-size: 14px;
          font-family: '思源黑体 Bold', '思源黑体';
          font-weight: 700;
          font-style: normal;
       }
       .b3{
           position: absolute;
           width:315px;height: 200px;
           top:40px;left:0px;
       }
       .b2{
           float: left;
        margin-left: 15px;
        margin-top:20px;
        width:60px;height: 50px;
         text-align: center;
       }
       
       .b2>p:nth-child(2){
            margin: 0px;
            font-size: 12px;
       }
</style>