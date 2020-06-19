<template>
    <div>
        <div class="car-list">
            <section>
                <header>
                    <h4>
                        <img src="../../assets/images/icon/car-logo.png">
                        <b>Mustang 2019款</b>
                    </h4>
                    <span>新能源汽车 5座</span>
                </header>
                <div class="content">
                    <div class="car-attr">
                        <div>
                            <div class="car-number">粤 B745N8</div>
                            <div class="distance active-distance-5">
                                <ul>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    <li></li>
                                    约<span>600</span>KM
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="carImg"><img src="../../assets/images/pic_001.jpg"></div>
                </div>
                <footer>
                    <a href="javascropt:void(0)">某停车场</a>
                </footer>
            </section>
        </div>
        <div class="car-list cars-details"  :style="'height:' + height">
             <section>
                 <div class="parking">
                     <span>某某停车场</span>
                 </div>
                <header>
                    <h4>
                        <img src="../../assets/images/icon/car-logo.png">
                        <b>Mustang 2019款</b>
                    </h4>
                    <span>新能源汽车 5座</span>
                </header>
                <div class="detailCarImg"><img src="../../assets/images/pic_001.jpg"></div>
                <div class="car-info">
                    <span>粤 B745N8</span>
                    <b>约<i>600</i>KM</b>
                </div>
                <div class="mileage-box">
                        <div class="mileage-bar">
                            <span></span>
                        </div>
                </div>
                <div class="car-tip">
                    <h4>取车约支付12.0元停车费，实际补贴12.0元</h4>
                </div>
                <div class="tip-content">
                    <ul>
                        <li>
                            <span>日租车</span>
                            <span>￥300/1天</span>
                        </li>
                        <li>
                            <span>3日租车</span>
                            <span>￥499.00/1天</span>
                        </li>
                        <li>
                            <span>5日租车</span>
                            <span>￥799.00/1天</span>
                        </li>
                        <li>
                            <span>小时租车</span>
                            <span>￥99.00/1天</span>
                        </li>
                    </ul>
                </div>
                <div class="rules">
                    <p>参保《全面保障服务》用车更放心</p>
                </div>
            </section>
        </div>
        <button class="ready-car">预约用车</button>
    </div>
</template>
<script>
export default {
    name:'swiperCar',
    data(){
        return{
             
        }
    },
    props:{
        height:{
            type:String,
            default:'257px'
        }
    },
    methods:{
      
    }
}
</script>
<style lang="scss">
    .car-list{
        // width:505px;
        height: 257px;
        overflow-y:auto;
        background: #fff;
        border-radius: 24px;
        padding:30px;
        margin:30px auto;
        margin-bottom:15px;
        @include webkit(box-shadow,0 0 18px #000);
        @include webkit(box-sizing,border-box);
        section header{
            width:100%;
            @extend %clearfix;
            h4{
                float: left;
                img{
                    display: inline-block;
                    vertical-align: middle;
                    margin-right:10px;
                }
                b{
                    display: inline-block;
                }
            }
        }
        section header span{
            float: right;
            line-height:27px;
        }
    }
    .content {
        width:100%;
        @extend %clearfix;
        .carImg{
            height: 120px;
            display: flex;
            align-items: center;
            & img{
                width:100%;
                float: right;
            }
        }
    }
    
    .car-attr{
        height: 120px;
        display: flex;
        float: left;
        align-items: center;
        .car-number{
            margin:10px 0;
            font-size:18px;
        }
        .distance ul li{
            width:5px;
            height: 24px;
            border-radius: 100px;
            background: #e1e1e1;
            display: inline-block;
            margin-right:2px;
        }
        .distance ul span{
            font-weight: bolder;
            font-size: 22px;
            padding:0 5px;
        }

        @for $i from 1 through 10 {    //这种方式只有知道li元素是固定的情况下 10 代表循环10个li元素 1 代表从第一个开始循环 
            .active-distance-#{$i} ul li:nth-child(-n+#{$i}){
                @include webkitA(background,linear-gradient(#32b2fb,#2b9add))
            }
        }
        
    }

    footer a{
        height: 45px;
        display: block;
        border-top:1px #ccc solid;
        color: $color-main;
        position:relative;
        line-height:45px;
        &:after{
            content: '';
            width: 8px;
            height: 8px;
            position: absolute;
            top:18px;
            right:0;
            display:block;
            border-top:1px #d6d7d9 solid;
            border-right:1px #d6d7d9 solid;
            @include webkit(transform,rotate(45deg));
        }
    }

    .cars-details{
        width: 100%;
        position: absolute;
        bottom:0;
        left: 0;
        .parking{
            padding-bottom:15px;
            border-bottom:1px #e1e1e1 solid;
            margin-bottom:7px;
            position: relative;
            span:after,span:before{
               content: '';
               width:15px;
               height: 15px;
               border-top:1px #ccc solid; 
               display: inline-block;
               position: absolute;
               cursor: pointer;
            }
            span:before{
                @include webkit(transform,rotate(45deg));
                right:0;
                top:7px
            }
             span:after{
                @include webkit(transform,rotate(-45deg));
                right:-10px;
                top:7px
            }
        }
        .detailCarImg{
            width:80%;
            margin:0 auto;
            img{
                width:100%
            }
        }
        .car-info{
            @extend %clearfix;
            width:100%;
            span{
                float: left;
            }
            b{
                float:right;
            }
        }
        .mileage-box{
            height: 35px;
            @include webkit(box-shadow,0 0 5px #e1e1e1);
            border-radius: 100px;
            position: relative;
            .mileage-bar{
                height: 8px;
                background: #e1e1e1;
                width:90%;
                border-radius: 100px;
                position: absolute;
                bottom: 0;
                top:0;
                left: 0;
                right: 0;
                margin: auto;
                span{
                    height: 8px;
                    background: $color;
                    width:80%;
                    border-radius: 100px;
                    position: absolute;
                    bottom: 0;
                    top:0;
                    left: 0;
                    margin: auto;
                }
            }
        }
        .car-tip{
            text-align: center;
            margin:10px 0;
        }
        .tip-content ul li{
            height: 40px;
            line-height: 40px;
            background: #f3f3f3;
            border-radius: 10px;
            margin-bottom:5px;
            padding:0 10px;
            span:nth-child(2){
                float: right;
            }
        }
        .rules{
            margin-top:10px;
        }
        
    }
    .ready-car{
            width: 150px;
            height: 44px;
            border-radius: 100px;
            background-color: #34393f;
            line-height: 44px;
            color: #fff;
            display: inline-block;
            position: absolute;
            bottom:-9px;
            left: 0;
            right: 0;
            z-index: 100;
            margin:auto;
            border:none;
        }
</style>