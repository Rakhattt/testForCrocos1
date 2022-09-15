<template>
    <section class="tabs_bg">
        <div class="container">
            <div class="tabs_wrapper">
                <div class="tabs_title">Отдых рядом с городом</div>
                <div class="tabs_subtitle">Коргалжынский заповедник</div>
                <div class="tabs_text">Коргалжынский государственный природный заповедник называют «жемчужиной края».</div>
                <a href="javascript:;" class="tab_arr">Подробнее</a>
            </div>
        </div>
        <div class="tabs_wrap">
           <div class="tabs_unit">
               <div class="tabs_blog">
                   <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner1 = true" @mouseleave="tabs_wrap_inner1 = false">
                       <div class="tabs_wrap_inner tabs_wrap_inner1"></div>
                   </div>
               </div>
               <div v-show="tabs_wrap_inner1" class="tabs_blog_hide">Коргалжынский заповедник</div>
           </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner2 = true" @mouseleave="tabs_wrap_inner2 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner2"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner2" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner3 = true" @mouseleave="tabs_wrap_inner3 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner3"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner3" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner4 = true" @mouseleave="tabs_wrap_inner4 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner4"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner4" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner5 = true" @mouseleave="tabs_wrap_inner5 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner5"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner5" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner6 = true" @mouseleave="tabs_wrap_inner6 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner6"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner6" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
            <div class="tabs_unit">
                <div class="tabs_blog">
                    <div class="tabs_wrap_img" @mouseover="tabs_wrap_inner7 = true" @mouseleave="tabs_wrap_inner7 = false">
                        <div class="tabs_wrap_inner tabs_wrap_inner7"></div>
                    </div>
                </div>
                <div v-show="tabs_wrap_inner7" class="tabs_blog_hide">Коргалжынский заповедник</div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Tabs",
        data() {
            return {
                tabs_wrap_inner1 : false,
                tabs_wrap_inner2:  false,
                tabs_wrap_inner3:  false,
                tabs_wrap_inner4:  false,
                tabs_wrap_inner5:  false,
                tabs_wrap_inner6:  false,
                tabs_wrap_inner7:  false,
            }
        },
    }
</script>

<style lang="less">
    .tabs_bg {
        background: center / cover no-repeat url("../assets/korgaljino.png");
        max-height: 800px;
        position: relative;
    }
    .tabs_wrapper {
        background: rgba(0, 0, 0, 0.27);
        backdrop-filter: blur(3px);
        padding: 200px 30px 200px 60px;
        width: 50%;
    }
    .tabs_title {
        font-weight: 600;
        font-size: 36px;
        line-height: 44px;
        color: #FFFFFF;
    }
    .tabs_subtitle {
        font-weight: 700;
        font-size: 48px;
        line-height: 59px;
        color: #FFFFFF;
        margin-top: 40px;
        margin-bottom: 5px;
    }
    .tabs_text {
        font-weight: 500;
        font-size: 16px;
        line-height: 25px;
        color: #FFFFFF;
        margin-bottom: 35px;
    }
    .tab_arr {
        font-weight: 500;
        font-size: 16px;
        line-height: 19px;
        letter-spacing: -0.03em;
        color: #FFFFFF;
        padding: 10px 45px 10px 25px;
        background: url(../assets/ar-right.svg) 80% center / 9px no-repeat;
        border: 1px solid #FFFFFF;
        border-radius: 25px;
        transition: .3s all;
        &:hover {
            border: 1px solid #011832;
            background-image: url("../assets/ar-right-hover.svg");
            color: #011832;
        }
    }
    .tabs_wrap {
        position: absolute;
        bottom: 10%;
        right: 5%;
        top: 10%;
    }
    .tabs_wrap_img {
        width: 70px;
        height: 70px;
        border-radius: 100%;
        /*background: linear-gradient(#83838373, #83838373);*/
        background-color: #000;
        transition: 0.4s all;
        padding: 10px;
        background-position-x: center;
        background-position-y: center;
        background-repeat: no-repeat;
        cursor: pointer;
        &:hover {
            background-color: #fff;
        }
        &:hover .tabs_wrap_inner{
            background-image: url("../assets/tabs_hover.svg");
        }
    }
    .tabs_wrap_inner {
        background-repeat: no-repeat;
        background-size: 40px;
        background-position-x: center;
        background-position-y: center;
        transition: 0.4s all;
        margin: 0 auto;
        width: 40px;
        height: 40px;
    }
    .tabs_wrap_inner1 {
        background-image: url(../assets/tab1.svg);
    }
    .tabs_wrap_inner2 {
        background-image: url(../assets/tab2.svg);
    }
    .tabs_wrap_inner2 {
        background-image: url(../assets/tab2.svg);
    }
    .tabs_wrap_inner3 {
        background-image: url(../assets/tab4.svg);
    }
    .tabs_wrap_inner4 {
        background-image: url(../assets/tab4.svg);
    }
    .tabs_wrap_inner5 {
        background-image: url(../assets/tab5.svg);
    }
    .tabs_wrap_inner6 {
        background-image: url(../assets/tab6.svg);
    }
    .tabs_wrap_inner7 {
        background-image: url(../assets/tab7.svg);
    }
    .tabs_blog {
        background: linear-gradient(#614f4f73, #614f4f73);
        border-radius: 100%;
        padding: 5px;
        z-index: 23;
        &:not(:last-child) {
            margin-bottom: 10px;
        }
    }
    .tabs_blog_hide {
        padding: 20px 150px 20px 35px;
        background: rgba(255, 255, 255, 0.8);
        backdrop-filter: blur(2px);
        border-radius: 45px 60px 50px 45px;
        font-weight: 500;
        font-size: 14px;
        line-height: 17px;
        color: #03B0CD;
        position: absolute;
        right: 25%;
        top: 0%;
        z-index: 0;
    }
    .tabs_unit {
        display: flex;
        flex-direction: row-reverse;
        position: relative;
    }
    .tabs_blog_hide {
        animation: hide 0.5s ease-in-out forwards;
    }
    @keyframes hide {
        0% {transform: translateX(-150%);}
        15% {transform: translateX(5%);}
        30% {transform: translateX(-5%);}
        45% {transform: translateX(3%);}
        60% {transform: translateX(-3%);}
        75% {transform: translateX(1%);}
        85% {transform: translateX(-1%);}
        100% {transform: translateX(0);}
    }
    /* media screen */
    @media screen and (max-width: 1500px) {
        .container {
            width: 1200px;
        }
        .tabs_subtitle {
            font-size: 45px;
            line-height: 48px;
            margin-top: 30px;
        }
        .tabs_title {
            font-size: 34px;
        }
        .tabs_wrap {
            bottom: 5%;
            top: 5%;
        }
    }

    @media screen and (max-width: 1350px) {
        .container {
            width: 1100px;
        }
    }

    @media screen and (max-width: 1200px) {
        .container {
            width: 1000px;
        }
    }

    @media screen and (max-width: 1100px) {
        .container {
            width: 900px;
        }
        .tabs_wrapper {
            padding: 150px 30px 150px 60px;
            width: 70%;
        }
        .tabs_subtitle {
            font-size: 40px;
            line-height: 40px;
            margin-top: 25px;
        }
        .tabs_title {
            font-size: 32px;
            line-height: 40px;
        }
        .tabs_wrap {
            bottom: 0%;
            right: inherit;
            top: inherit;
            display: flex;
            left: 10%;
        }
        .tabs_blog:not(:last-child) {
            margin-bottom: 0;
            margin-right: 10px;
        }
        .tabs_blog_hide {
            display: none;
        }
    }

    @media screen and (max-width: 1000px) {
        .container {
            width: 800px;
        }
        .tabs_wrapper {
            padding: 120px 30px 120px 60px;
            width: 100%;
        }
        .tabs_subtitle {
            font-size: 36px;
        }
        .tabs_title {
            font-size: 30px;
        }
        .tabs_text {
            font-size: 15px;
        }
    }

    @media screen and (max-width: 880px) {
        .container {
            width: 700px;
        }
        .tabs_wrap_img {
            width: 60px;
            height: 60px;
        }
    }

    @media screen and (max-width: 780px) {
        .container {
            width: 600px;
        }
    }

    @media screen and (max-width: 680px) {
        .container {
            width: 500px;
        }
        .tabs_wrapper {
            padding: 80px 30px 100px 60px;
        }
        .tabs_subtitle {
            font-size: 32px;
            line-height: 34px;
            margin-top: 20px;
        }
        .tabs_title {
            font-size: 28px;
            line-height: 30px;
        }
        .tabs_wrap_img {
            width: 50px;
            height: 50px;
        }
        .tabs_wrap_inner {
            width: 30px;
            height: 30px;
            background-size: 30px;
        }
    }

    @media screen and (max-width: 570px) {
        .container {
            width: 100%;
            padding-left: 20px;
            padding-right: 20px;
        }
        .tabs_wrap_img {
            width: 40px;
            height: 40px;
        }
        .tabs_wrap_inner {
            width: 20px;
            height: 20px;
            background-size: 20px;
        }
        .tabs_title {
            font-size: 24px;
        }
        .tabs_subtitle {
            font-size: 26px;
            line-height: 30px;
        }
        .tabs_wrap {
            left: 0;
        }
    }

    @media screen and (max-width: 500px) {

    }

    @media screen and (max-width: 400px) {
        .tabs_wrap_img {
            width: 32px;
            height: 32px;
        }
        .tabs_wrap_inner {
            width: 20px;
            height: 20px;
            background-size: 20px;
        }
    }
</style>
