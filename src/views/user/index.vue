<template>
    <div>
       <div class="user_wrap">
           <img src="../../assets/images/icon/uesr_03.png" alt="">
           <div class="user_info">
               <div>
               <span>409019683@qq.com</span>
               <p>文明驾驶分0</p>
               </div>
           </div>
       </div>
       <div class="user_list">
            <ul>
                <router-link to="">
                    <i class="icon icon-account"></i>
                    <span>我的账户</span>
                </router-link>
                <router-link to="">
                    <i class="icon icon-order"></i>
                    <span>租车订单</span>
                </router-link>
                <router-link to="">
                    <i class="icon icon-attestation"></i>
                    <span>实名认证</span>
                </router-link>
                <router-link to="">
                    <i class="icon icon-security"></i>
                    <span>安全设置</span>
                </router-link>
                <router-link to="">
                    <i class="icon icon-center"></i>
                    <span>帮助中心</span>
                </router-link>
            </ul>
        </div>
        <div class="login_out">
            <button>退出</button>
        </div>
    </div>
</template>
<script>
export default {
    name:'Users',
    data(){
        return{

        }
    }
}
</script>
<style lang="scss">
    .user_wrap{
        height: 255px;
        display: flex;
        align-items: center;
        img{
            margin:0 20px 0 40px;
        }
        .user_info{
            height: 100px;
            flex: 1;
            color:#909090;
            display: flex;
            align-items: center;
            span{
                padding:10px 0;
                display: inline-block;
                font-size:18px;
            }
            p{
                width:117px;
                background: #0f9ef0;
                border-radius: 100px;
                color:#fff;
                height: 27px;
                line-height: 27px;
                text-align: center;
            }
        }
    }
    .user_list ul a{
        display: block;
        color: #909090;
        border-bottom:1px #3a3f45 solid;
        padding:20px 0;

        i.icon{
            width:26px;
            height: 26px;
            display: inline-block;
            border-radius: 100px;
            vertical-align: middle;
            margin: 0 20px 0 32px;
        }
    }
    .login_out{
        position: absolute;
        bottom:60px;
        left:0;
        right: 0;
        margin:auto;
         width:165px;
        button{
            width:165px;
            height: 58px;
            background: #2d3339;
            border: none;
            border-radius: 100px;
            color: #fff;
            font-size: 18px;
            outline: none;
            cursor: pointer;
        }
    }
</style>