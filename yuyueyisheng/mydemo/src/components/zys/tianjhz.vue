<template>
    <div>
        <div class="u1">
            <img :src="q" alt="" class="u2">
            <img :src="w" alt="" class="u3">
        </div>
        <div class="u4" >
            <div class="u5" @click="aaa" >
                <img :src="e" alt="">
                <span>添加患者</span>
            </div>
            <span @click="bbb">保存</span>
        </div>
        <div class="u6">
            <div class="u7">
                <span>姓名</span>
                <input type="text" placeholder="请输入真实姓名">
            </div>
            <div class="u7">
                <span>身份证号</span>
                <input type="text" placeholder="请输入身份证号">
            </div>
            <div class="u8">
                <span>性别</span>
                <div>
                    <div @click="qwe">
                        <div><img :src="r" alt="" v-if="num==1"></div> 
                        <span>男</span>
                    </div>
                    <div @click="asd">
                        <div><img :src="r" alt="" v-if="num==2"></div> 
                        <span>女</span>
                    </div>
                </div>
            </div>
            <div class="u9">
                <span>出生年月</span>
                <div @click="openPicker">
                    <input type="text" placeholder="请选择出生年月">
                    <img :src="t" alt="">
                </div>
            </div>
            <div class="u9">
                <span>地址</span>
                <div>
                    <input type="text" placeholder="请选择你的地址">
                    <img :src="t" alt="">
                </div>
            </div>
        </div>
        <mt-datetime-picker
            v-model="pickerVisible"
            ref="picker"
            type="date"
            year-format="{value} 年"
            month-format="{value} 月"
            date-format="{value} 日"
            @confirm="open">
        </mt-datetime-picker>
    </div>
</template>
<script>
export default {
    data(){
        return{
             pickerVisible:new Date(),
             num:1
        }
    },
    props:{
        q:{default:""},
        w:{default:""},
        e:{default:""},
        r:{default:""},
        t:{default:""},
    },
    methods:{
        openPicker () {
            this.$refs.picker.open()
        },
        qwe(){
            this.num=1
        },
        asd(){
            this.num=2
        },
        open(value){
            console.log(value);
            this.year=value.getFullYear();
            this.month=value.getMonth()+1;
            this.data=value.getDate();
            
            var span=document.querySelector(".u9 input")
            span.value=this.year+"年"+this.month+"月"+this.data+"日"
        },
        aaa(){
            window.history.go(-1)
        },
        bbb(){
            this.$toast({
            message:"保存成功", //消息
            position:"center",     //位置
            duration:2000,      //时间
            });    
            this.$router.push("Home7")
        }
    }
}
</script>
<style scoped>
    .u1{
        width:360px;
        height:44px;
        position:fixed;
        top:4px;
        background-color:#fff;
        z-index:2;
    }
    .u2{
        position: absolute;
        left: 0px;
        top: 0px;
        width: 365px;
        height: 44px;
    }
    .u3{
        border-width: 0px;
        position: absolute;
        left: 50%;
        top: -1px;
        margin-left:-85px;
        width: 170px;
        height: 30px;
    }
   .u4{
        width:325px;
        margin:56px auto 0px;
       display:flex;
       justify-content:space-between;
       font-family: '思源黑体';
        font-weight: 400;
        font-style: normal;
        font-size: 14px
    }
    .u4>.u5{
        display:flex;
        align-items:center;
    }
    .u4>span{
        color:#00C8AB;
    }
    .u5>span{
        margin-left:10px;
        font-family: '思源黑体 Bold', '思源黑体';
        font-weight: 700;
        font-style: normal;
        font-size: 18px;
        color:#333;
    }
    .u5>img{
        font-family: '思源黑体';
        font-weight: 400;
        font-style: normal;
        font-size: 14px
    }
    .u6{
        width:325px;
        margin:0px auto;
    }
    .u6>div{
        margin-top:30px;
    }
    .u7,.u8,.u9{
        display:flex;
        justify-content:space-between;
        font-family: '思源黑体';
        font-weight: 400;
        font-style: normal;
        font-size: 14px;
        color:#333;
        align-items:center;
    }

    .u7>input{
        width:112px;
        height:30px;
        border:0;
        outline:none;
        background-color:rgba(0,0,0,0.03);
    }
    .u8>div,.u8>div>div{
        display:flex;
    }
    .u8>div>div>div{
        width:18px;
        height:18px;
        border:1px solid #e8e8e8;
        border-radius:50%;
    }
    .u8>div>div{
        margin-left:30px;
    }
    .u8>div>div>div>img{
        width:18px;
        height:18px;
    }
    .u8>div>div>div{
        margin-right:10px;
    }
    .u9>div{
        display:flex;
        align-items:center;
    }
    .u9>div>img{
        width:7px;
        height:12px;
    }
    .u9>div>input{
        width:120px;
        height:30px;
        outline:none;
        border:0px;
    }
</style>