<template>
    <div class="boxContainer">
        <Cars />
        <Map />
        <NavBar />
        <div  :class="['userContainer' , show ? 'active':'']">
            <router-view />
        </div>
      </el-amap>
    </div>
</template>
<script>
import Map from "../map";
import Cars from "../cars";
import NavBar from "@c/navBar";
export default {
    name:'Index',
    components:{ Map , Cars , NavBar},
    data(){
        return {
            // show:false
        }
    },
    computed:{
        show(){
            let route = this.$route;
            return route.name === 'Index' ? false : true
        }
    }
    // watch:{
    //     $route:{
    //         handler:function(newVal, oldVal){
    //             console.log(newVal)
    //             this.show = newVal.name === "Index" ? false : true;
    //         }
    //     },
    //     deep:true
    // }
}
</script>
<style lang="scss">
    .userContainer{
        position: fixed;
        width:410px;
        top:0;
        right:-410px;
        bottom:0;
        background-color: #34393f;
        z-index:9999;
        transition: all 0.3s ease;
    }
    .active{
        right:0;
    }
</style>