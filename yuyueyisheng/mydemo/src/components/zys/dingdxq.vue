<template>
    <div>
        <div class="m1">
            <img :src="q" alt="" class="m2">
            <img :src="w" alt="" class="m3">
        </div>
        <div class="m4">
            <div class="m5" @click="op">
                <img :src="e" alt="">
                <span>订单详情</span>
            </div>
        </div>
        <div class="m6">
            <p><span style="font-family:'思源黑体 Bold', '思源黑体 Regular', '思源黑体';font-weight:700;">订单待接诊</span></p>
            <p><span style="font-family:'思源黑体';font-weight:400;font-size:12px;">订单支付成功，正在等待医生接诊</span></p>
        </div>
        <div class="m7">
            <span style="font-family:'思源黑体 Bold', '思源黑体 Regular', '思源黑体';font-weight:700;">订单类型</span>
            <span style="font-family:'思源黑体';font-weight:400;">专家问诊</span>
        </div>
        <div class="m8">
            <img :src="a" alt="">
            <div>
                <div>
                    <span style="margin-top:30px;">张清北</span>
                    <span>副主任医师</span>
                </div>
                <p><span>北京协和医院  儿科</span></p>
            </div>
            <img :src="s" alt="">
        </div>
        <div class="m9">
            <div><span>咨询内容</span></div>
            <div>
                <span>患者信息</span>
                <span>    罗敏君  男   32岁</span>
            </div>
            <div>
                <span>患病时间</span>
                <span>    一周内</span>
            </div>
            <div>
                <span>就诊情况</span>
                <span>    未去医院就诊过</span>
            </div>
            <div>
                <span>病情描述</span>
                <span>    腹痛腹泻  胃部有些痉挛</span>
            </div>
        </div>
        <div class="m9">
            <div><span>订单详情</span></div>
            <div>
                <span>订单编号</span>
                <span>    4025201907040253666</span>
            </div>
            <div>
                <span>下单时间</span>
                <span>    2019-07-08  09:55:54</span>
            </div>
            <div>
                <span>应付款</span>
                <span>&nbsp;&nbsp;&nbsp;¥49.00</span>
            </div>
            <div>
                <span>优惠券</span>
                <span>&nbsp;&nbsp;&nbsp;-¥10.00</span>
            </div>
            <div>
                <span>实际支付</span>
                <span>    ¥39.00</span>
            </div>
            <div>
                <span>支付时间</span>
                <span>    2019-07-08  09:55:54</span>
            </div>
            <div>
                <span>支付方式</span>
                <span>    微信支付</span>
            </div>
        </div>
        <div class="m10">
            <div class="m11" @click="er">
                <span>取消订单</span>
            </div>
        </div>
        <div class="m12"></div>
    </div>
</template>
<script>
export default {
    data(){
        return{
        }
    },
    props:{
        q:{default:""},
        w:{default:""},
        e:{default:""},
        a:{default:""},
        s:{default:""},
    },
    methods:{
        er(){
            this.$messagebox.confirm("是否删除订单")
            .then(action=>{})
            .catch(err=>{})
        },
        op(){
            window.history.go(-1)
        }
    }
}
</script>
<style scoped>
    .m1{
        width:360px;
        height:44px;
        position:fixed;
        top:4px;
        background-color:#fff;
        z-index:10;
    }
    .m2{
        position: absolute;
        left: 0px;
        top: 0px;
        width: 365px;
        height: 44px;
    }
    .m3{
        border-width: 0px;
        position: absolute;
        left: 50%;
        top: -1px;
        margin-left:-85px;
        width: 170px;
        height: 30px;
    }
   .m4{
        width:100%;
        height:80px;
        margin:0px auto 0px;
        padding:0px 25px;
        display:flex;
        justify-content:space-between;
        position:fixed;
        top:0px;
        box-sizing:border-box;
        background-color:#fff;
        z-index:2;
    }
    .m4>span{
        font-family: '思源黑体';
        font-weight: 400;
        font-style: normal;
        font-size: 14px;
        color:#333;
        margin-top:56px;
    }
    .m4>.m5{
        display:flex;
        align-items:center;
        margin-top:50px;
    }
    .m5>span{
        margin-left:10px;
        font-family: '思源黑体 Bold', '思源黑体';
        font-weight: 700;
        font-style: normal;
        font-size: 18px;
        color:#333;
    }
    .m5>img{
        font-family: '思源黑体';
        font-weight: 400;
        font-style: normal;
        font-size: 14px
    }
    .m6{
        width:100%;
        height:72px;
        background-color: rgba(0, 200, 170, 1);
        margin-top:90px;
        color:#fff;
    }
    .m6:before{
        content:"";
        display:table;
    }
    .m6>p:first-child>span{
        font-size:24px;
    }
    .m6>p{
        margin:0;
    }
    .m6>p:first-child{
        margin-top:9px;
    }
    .m7,.m9{
        width:325px;
        margin:30px auto 0px;
        text-align:left;
    }
    .m7>span{
        font-size: 14px;
        color:#333;
        margin-right:10px;
    }
    .m8{
        width:325px;
        margin:0px auto;
        display:flex;
        justify-content:space-between;
        align-items:center;
        height:81px;
    }
    .m8>div{
        width:250px;
        height:100%;
        text-align:left;
    }
    .m8>div>p{
        margin:0px;
        font-size: 12px;
        color: #666666;
    }
    .m8>div>div{
        margin-top:22px;
    }
    .m8>div>div>span:first-child{
        font-family: '思源黑体 Bold', '思源黑体 Regular', '思源黑体';
        font-weight: 700;
        font-size:14px;
    }
    .m8>div>div>span:last-child{
        font-family: '思源黑体 Bold', '思源黑体 Regular', '思源黑体';
        font-size:14px;
    }
    .m9>div:first-child{
        font-family: '思源黑体 Bold', '思源黑体 Regular', '思源黑体';
        font-weight: 700;
        color:#333;
        font-size:14px;
    }
    .m9>div:not(:first-child)>span:first-child{
        color: #CCCCCC;
        font-size: 12px;
        font-weight: 400;
    }
    .m9>div:not(:first-child)>span:not(:first-child){
        color: #333;
        font-size: 12px;
        font-weight: 400;
        margin-left:10px;
    }
    .m9>div{
        margin-top:10px;
    }
    .m10{
        width:100%;
        height:80px;
        background-color:#fff;
        position:fixed;
        left:0px;
        bottom:0px;
    }
    .m11{
        width:68px;
        height:24px;
        border:1px solid rgba(0, 200, 170, 1);
        color:rgba(0, 200, 170, 1);
        border-radius:30px;
        font-size:12px;
        line-height:24px;
        margin-left:285px;
        margin-top:10px;
    }
    .m12{
        margin-top:110px;
    }
</style>