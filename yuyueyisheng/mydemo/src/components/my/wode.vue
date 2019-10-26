<template>
<!-- import func from './vue-temp/vue-editor-bridge'; -->
           <div class='bt'>
             
                <div class='b1'>
                  <span class='a3'><font>我的</font></span>
                  <img @click='xiaoxi' class='a4' :src='c'>
                </div>
                <div class='a5'>
                  <img :src='d'>
                </div>
                 
                 <span class='a6' id="uname" >{{name}}</span>
                 <div class='a7'>
                <div class='a8'>
                    <p style='margin:0'>150</p>
                    <p style='margin:0'>收藏</p>
                 </div>
                 <div class='a9'>
                 <p style='margin:0'>23</p>
                    <p style='margin:0'>关注医生</p>
                 </div>
                 <div class='a10'>
                 <p style='margin:0'>3</p>
                    <p style='margin:0'>优惠卷</p>
                 </div>
                </div>
           </div> 
</template>
<script>
    export default{

        data(){
            return{
                    name:""
            }
        },
        created:function(){
            this.se();
        },
      props:{
          a:{default:''},
          b:{default:''},
          c:{default:''},
          d:{default:''}
      },
      methods:{
          
          xiaoxi(){
              this.$router.push('/xiaoxi')
          },
          se(){
              this.axios("sename").then(res=>{
                  //console.log(res.data)
                  var span=document.getElementById("uname");
                  var button=document.getElementById("login1")
                  if(res.data.code==1){
                      span.style="display:block";
                      
                     this.name=res.data.data[0].uname;
                  }else{
                      span.style="display:none";
                     
                  }
              })
          }

      }
    }
</script>
<style scoped>
        
      .bt{
         position:relative;
         width:100%;
         height:280px;
        background:rgba(0, 200, 170, 1);
        z-index:0;
         overflow:hidden;
      }
      .a1{
          
          width:365px;height:44px;
          left:0;
      }
      .a2{
          position:fixed;
          top:-1px;left:50%;
          margin-left:-90px;
          z-index:1;
   
      }
      .b1{
          margin-top:44px;
          position:relative;
        display:flex;
        justify-content:space-between;
      }
      .a3{
         display:flex;
          font-family: '思源黑体 Bold', '思源黑体';
          font-weight: 700;
          font-size: 24px;
          color: #FFFFFF;
          margin-left:24px;
      }
       .a4{
           display:flex;
           margin-right:24px;
           width:18px;height:22px;
       }
       .a4:hover{
            cursor:pointer;
       }
       .a5{
           position:relative;
           left:24px;top:25px;
           background:#fff;
           width:50px;height:50px;
           border-radius:50%; 
       }
       .a5>img{
           position:absolute;
           top:50%;margin-top:-10px;
           left:50%;margin-left:-11px;
       }
       .a6{
           position:relative;
            font-family:'思源黑体 Bold', '思源黑体';
            font-weight: 700;
            font-size: 16px;
            color: #FFFFFF;
            right:40px;bottom:10px;
        }
        .a7{
            margin-top:20px;
            display:flex;
             justify-content:space-around;
        }
        .a8,.a9,.a10{
            width:43px;height:35px;
        }
         .a8>p,.a9>p,.a10>p{
             width:60px;
             font-size:13px;
             color:#fff;
             font-family: '思源黑体';
            font-weight: 400;
         }
</style>