<template>
    <div class="aMap">
        <el-amap ref="map" vid="amapDemo"  :keyboardEnable="keyboardEnable" class="amap-demo">
      </el-amap>
    </div>
</template>
<script>
import { lazyAMapApiLoaderInstance } from 'vue-amap';
export default {
    name:'Map',
    data(){
        return {
            map:null,
            // zoom:10,
            // center:[121.59996, 31.197646],
            keyboardEnable:true
        }
    },
    mounted(){
        lazyAMapApiLoaderInstance.load().then(() => {
            this.map = new AMap.Map('amapDemo', {
                center: new AMap.LngLat(116.298829,39.905547),
                zoom:10,
            });
        });
    }
}
</script>
<style lang="scss">
    .aMap{
        height: 100vh;
    }
</style>