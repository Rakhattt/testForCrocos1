<template>
    <section class="main">
        <div class="main_vh">
            <div class="container">
                <div class="pt-x">
                    <div class="main_jpg"><img src="../assets/astana.svg" alt="Astana"></div>
                </div>
                    <div class="main_blog">
                        <div class="main_blog_item">
                            <a target="_blank" href="javascript:;"><img src="../assets/ast1.svg" alt=""></a>
                            <div class="main_blog_title">Где остановиться?</div>
                            <div class="main_blog_subtitle">отели, хостелы...</div>
                        </div>
                        <div class="main_blog_item">
                            <a target="_blank" href="javascript:;"><img src="../assets/ast2.svg" alt=""></a>
                            <div class="main_blog_title">Где поесть?</div>
                            <div class="main_blog_subtitle">рестораны, кафе...</div>
                        </div>
                        <div class="main_blog_item">
                            <a target="_blank" href="javascript:;"><img src="../assets/ast3.svg" alt=""></a>
                            <div class="main_blog_title">Куда сходить?</div>
                            <div class="main_blog_subtitle">Театры, кино...</div>
                        </div>
                        <div class="main_blog_item">
                            <a target="_blank" href="javascript:;"><img src="../assets/ast4.svg" alt=""></a>
                            <div class="main_blog_title">Что посмотреть?</div>
                            <div class="main_blog_subtitle">Музеи, байтерек...</div>
                        </div>
                    </div>
            </div>
        </div>
    </section>
</template>

<script>

    export default {
        name: "Main",
        data() {
            return {
            }
        },
        methods: {
        },
    }
</script>

<style lang="less">
    .main {
        height: 100vh;
        overflow: hidden;
    }
    .main_vh {
        height: 100%;
        background: center / cover no-repeat url("../assets/main_bg.png");
    }
    .container {
        width: 1350px;
        margin: 0 auto;
    }
    .pt-x {
        padding: 200px 0;
    }
    .main_jpg {
        width: 860px;
        height: 220px;
        margin: 0 auto;
        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .main_blog {
        display: flex;
        flex-wrap: wrap;
        .main_blog_item:not(:last-child) {
            margin-right: 2%;
        }
    }
    .main_blog_item {
        width: 23%;
        a {
            display: block;
            width: 125px;
            height: 125px;
            margin: 0 auto;

            img {
                display: block;
                width: 100%;
                height: 100%;
                object-fit: contain;
                border-radius: 100%;
                background: linear-gradient(#83838373, #83838373);
                padding: 5px;
                box-shadow: 0 -4px 4px rgba(0,0,0,0.3), 0 4px 4px rgba(0,0,0,0.3);
                transition: .4s all;
                &:hover {
                    background: linear-gradient(#00D1FF, #00D1FF);
                    box-shadow: 0 -4px 4px #00d1ff, 0 4px 4px #00d1ff;
                }
            }
        }
    }
    .main_blog_title {
        font-weight: 700;
        font-size: 17px;
        line-height: 21px;
        text-transform: uppercase;
        color: #FFFFFF;
        text-align: center;
        margin-top: 25px;
    }
    .main_blog_subtitle {
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: #FFFFFF;
        text-align: center;
    }
    /* media screen */
    @media screen and (max-width: 1500px) {
        .container {
            width: 1200px;
        }

    }

    @media screen and (max-width: 1350px) {
        .container {
            width: 1100px;
        }
        .main_jpg {
            width: 650px;
            height: 160px;
        }
        .main_blog_item a {
            width: 110px;
            height: 110px;
        }
        .pt-x {
            padding: 170px 0;
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
    }

    @media screen and (max-width: 1000px) {
        .container {
            width: 800px;
        }
        .main_jpg {
            width: 550px;
            height: 140px;
        }
        .main_blog_title {
            font-size: 16px;
            margin-top: 20px;
        }
    }

    @media screen and (max-width: 880px) {
        .container {
            width: 700px;
        }
        .main_blog_title {
            font-size: 15px;
            margin-top: 15px;
        }
        .main_blog_title {
            font-size: 15px;
            margin-top: 15px;
        }
    }

    @media screen and (max-width: 780px) {
        .container {
            width: 600px;
        }
        .main_blog .main_blog_item:nth-child(3) {
            display: none;
        }
        .main_blog .main_blog_item:nth-child(4) {
            display: none;
        }
        .main_blog_item {
            width: 47%;
        }
    }

    @media screen and (max-width: 680px) {
        .container {
            width: 500px;
        }
        .main_jpg {
            width: 470px;
            height: 100px;
        }
        .pt-x {
            padding: 150px 0;
        }
    }

    @media screen and (max-width: 570px) {
        .container {
            width: 100%;
            padding-left: 20px;
            padding-right: 20px;
        }
        .main_jpg {
            width: 350px;
            height: 90px;
        }
    }

    @media screen and (max-width: 500px) {
        .main_jpg {
            width: 280px;
            height: 70px;
        }
    }

    @media screen and (max-width: 400px) {

    }
</style>