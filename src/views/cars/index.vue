<template>
    <div class="car-wraper">
        <swiper class="swiper" :options="swiperOption">
            <swiper-slide><SwiperCar height="600px"/></swiper-slide>
            <swiper-slide><SwiperCar height="600px"/></swiper-slide>
            <swiper-slide><SwiperCar /></swiper-slide>
            <swiper-slide><SwiperCar /></swiper-slide>
            <swiper-slide><SwiperCar /></swiper-slide>
        </swiper>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
    </div>
</template>
<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import SwiperCar from '@c/swiperCar';
export default {
    name:'carsList',
    components: {
      Swiper,
      SwiperSlide,
      SwiperCar
    },
    data(){
        return{
           swiperOption: {
                slidesPerView: 3,
                spaceBetween: 30,
                navigation: {
                    nextEl: '.swiper-button-next',
                    prevEl: '.swiper-button-prev'
                }
            }
        }
    },
    methods:{
        
    }
}
</script>
<style lang="scss">
    .car-wraper{
        position: fixed;
        bottom:60px;
        left: 0;
        right:0;
        z-index: 11;
        .swiper-container{
            overflow: inherit;
        }
    }
    .swiper{
        width:85%;
        padding:0 15px;
    }
    .car-wraper .swiper-button-prev,.car-wraper .swiper-button-next{
        width:60px;
        height: 100px;
        border-radius: 100px;
        background: #fff;
        -webkit-appearance:none;
        outline:none;
        @include webkit(box-shadow,0 0 18px 0 rgba(0,0,0,0.2));
    }
</style>