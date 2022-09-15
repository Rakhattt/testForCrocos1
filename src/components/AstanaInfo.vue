<template>
    <section class="bg">
        <div class="container">
            <div class="ast_wrapper">
                <div class="ast_unit"><img src="../assets/ast_unit.png" alt=""></div>
                <div class="ast_block">
                    <div class="ast_block_inner">
                        <div class="ast_blog_title">Добро пожаловать в Астану</div>
                        <div class="ast_blog_subtitle">Астана - столица независимого Казахстана. Это молодой, современный, комфортный и динамичный город в котором каждый человек почувствует гостеприимность и радушие столицы.</div>
                    </div>
                        <div class="ast_blog">
                            <div class="ast_blog_item">
                                <div class="ast_blog_item_img"><img src="../assets/ast_item1.svg" alt=""></div>
                                <div class="ast_blog_item_title">достопримечательностей</div>
                            </div>
                            <div class="ast_blog_item">
                                <div class="ast_blog_item_img"><img src="../assets/ast_item2.svg" alt=""></div>
                                <div class="ast_blog_item_title">объектов питания</div>
                            </div>
                            <div class="ast_blog_item">
                                <div class="ast_blog_item_img"><img src="../assets/ast_item3.svg" alt=""></div>
                                <div class="ast_blog_item_title">доступных мероприятий</div>
                            </div>
                        </div>
                </div>
            </div>
        </div>
        <div class="ast_pos"><img src="../assets/ast-icon.svg" alt=""></div>
    </section>
</template>

<script>
    export default {
        name: "AstanaInfo"
    }
</script>

<style lang="less">
    .bg {
        background: center / cover no-repeat url("../assets/welcome_bg.png");
        position: relative;
        padding-top: 60px;
        padding-bottom: 340px;
    }
    .ast_pos {
        position: absolute;
        bottom: 90px;
        right: 20px;
        width: 110px;
        height: 110px;
        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }
    .ast_wrapper {
        display: flex;
        flex-wrap: wrap;
    }
    .ast_unit {
        position: absolute;
        width: 50%;
        flex-shrink: 0;
        overflow: hidden;
        top: 0;
        left: 0;
        margin-top: 150px;
        z-index: 0;
        height: 550px;
        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .ast_block {
    }
    .ast_block_inner {
        width: 48%;
        margin-left: auto;
    }
    .ast_blog_title {
        font-weight: 800;
        font-size: 46px;
        line-height: 56px;
        display: flex;
        align-items: center;
        text-transform: uppercase;
        color: #FFFFFF;
    }
    .ast_blog_subtitle {
        font-weight: 600;
        font-size: 18px;
        line-height: 30px;
        color: #FFFFFF;
    }
    .ast_blog {
        display: flex;
        flex-wrap: wrap;
        margin-top: 30px;
        width: 48%;
        margin-left: auto;
        .ast_blog_item:not(:last-child) {
            margin-right: 2%;
        }
    }
    .ast_blog_item {
        width: 31%;
    }
    .ast_blog_item_img {
        height: 45px;
        img {
            display: block;
            height: 100%;
            object-fit: contain;
        }
    }
    .ast_blog_item_title {
        font-weight: 600;
        font-size: 14px;
        line-height: 100%;
        color: #FFFFFF;
        margin-top: 10px;
    }
    /* media screen */
    @media screen and (max-width: 1500px) {
        .container {
            width: 1200px;
        }
        .bg {
            padding-bottom: 300px;
        }
        .ast_blog_title {
            font-size: 42px;
        }
        .ast_blog_item_img {
            height: 40px;
        }
    }

    @media screen and (max-width: 1350px) {
        .container {
            width: 1100px;
        }
        .ast_block_inner {
            width: 100%;
            margin-left: 0;
        }
        .ast_blog {
            flex-direction: column;
            .ast_blog_item:not(:last-child) {
                margin-right: 0;
                margin-bottom: 30px;
            }
        }
        .bg {
            padding-bottom: 210px;
        }
    }

    @media screen and (max-width: 1200px) {
        .container {
            width: 1000px;
        }
        .ast_unit {
            height: 430px;
        }
        .bg {
            padding-bottom: 80px;
        }
        .ast_blog_title {
             font-size: 38px;
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
        .ast_blog_title {
            font-size: 34px;
        }
        .ast_blog_subtitle {
            font-size: 17px;
        }
        .ast_blog_item {
            width: 100%;
        }
        .ast_blog_item_img {
            height: 35px;
        }
    }

    @media screen and (max-width: 880px) {
        .container {
            width: 700px;
        }
        .ast_blog_title {
            font-size: 30px;
        }
        .ast_blog_subtitle {
            font-size: 16px;
            line-height: 25px;
        }
        .ast_unit {
            height: 340px;
        }
        .ast_blog_item_img {
            height: 30px;
        }
        .ast_pos {
            display: none;
        }
    }

    @media screen and (max-width: 780px) {
        .container {
            width: 600px;
        }
        .ast_blog_title {
            font-size: 28px;
            line-height: 36px;
        }
    }

    @media screen and (max-width: 680px) {
        .container {
            width: 500px;
        }
        .bg {
            padding-bottom: 40px;
            padding-top: 40px;
        }
        .ast_unit {
            height: 250px;
        }
    }

    @media screen and (max-width: 570px) {
        .container {
            width: 100%;
            padding-left: 20px;
            padding-right: 20px;
        }
        .ast_blog_subtitle {
            font-size: 15px;
        }
        .ast_blog_title {
         font-size: 24px;
        }
        .ast_unit {
            width: 70%;
        }
        .ast_block {
            z-index: 23;
        }
    }

    @media screen and (max-width: 500px) {
        .ast_blog {
            margin-left: 0;
        }
    }

    @media screen and (max-width: 400px) {

    }
</style>
