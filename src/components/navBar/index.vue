<template>
    <div>
        <div class="navBarContainer">
            <ul>
                <li><i class="icon icon-help"></i></li>
                <li><i class="icon icon-search"></i></li>
                <li class="select-cars"><a href="javascript:void(0)">选择车辆</a></li>
                <li><i class="icon icon-location"></i></li>
                <li><i class="icon icon-user" @click="user"></i></li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    name:'navBar',
    data(){
        return{

        }
    },
    mounted(){
        
    },
    methods:{
      user(){
        this.$router.push({
            name:"User"
        })
      }
    }
}
</script>
<style lang="scss">
    .navBarContainer{
        width:100%;
        position: fixed;
        text-align: center;
        left: 0;
        bottom: 86px;
        z-index:10;
        ul li{
            display: inline-block;
            margin: 0 10px;
            &.select-cars a{
               width: 100px;
               height: 44px;
               border-radius: 100px;
               background-color:$color-main;   
               line-height:44px;   
               color:#fff;
               display: inline-block;     
            }
            .icon{
                vertical-align: middle;
            }
        }
    }
</style>