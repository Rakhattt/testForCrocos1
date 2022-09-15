<template>
    <section class="pad-x">
        <div class="container">
            <div class="visit_wrap">
                <div class="visit_wrap_blog">
                    <div class="visit_wrap_blog_title">#Astana</div>
                    <div class="visit_wrap_blog_subtitle">6 причин посетить город</div>
                </div>
                <a href="javascript:;" class="arr_right">Подробнее</a>
            </div>
            <div class="visit_wrapper">
                <div class="visit_block">
                    <div class="visit_block_img visit_block_img1"><img src="../assets/visit1.jpg" alt=""></div>
                    <div class="visit_block_title mr-25-15">Достопримечательности</div>
                    <div class="visit_block_subtitle">Футуристический город посреди степи — левый берег, олицетворяющий техногенное будущее.</div>
                </div>
                <div class="visit_block flex-direction">
                    <div class="visit_block_title order-1">Самый большой шатёр в мире</div>
                    <div class="visit_block_subtitle mr-15-25 order-0 ">ТРЦ Хан Шатыр является первым и единственным лайфстайл-центром, который объединяет шопинг и развлечения мирового уровня под одной крышей.</div>
                    <div class="visit_block_img visit_block_img2 order-2"><img src="../assets/visit2.jpg" alt=""></div>
                </div>
                <div class="visit_block">
                    <div class="visit_block_img visit_block_img3"><img src="../assets/visit3.jpg" alt=""></div>
                    <div class="visit_block_title mr-25-15">Уникальная архитектура</div>
                    <div class="visit_block_subtitle">Самая молодая и динамично развивающаяся столица стран СНГ. Возможно, именно поэтому архитектура города столь необычна и поразительна.</div>
                </div>
                <div class="visit_block">
                    <div class="visit_block_img visit_block_img4"><img src="../assets/visit4.jpg" alt=""></div>
                    <div class="visit_block_title mr-25-15">Гостеприимство</div>
                    <div class="visit_block_subtitle">Если вы заблудились, местные никогда не откажут в помощи. Дружелюбие казахов не знает границ.</div>
                </div>
                <div class="visit_block">
                    <div class="visit_block_img visit_block_img5"><img src="../assets/visit5.jpg" alt=""></div>
                    <div class="visit_block_title mr-25-15">Самая большая опера</div>
                    <div class="visit_block_subtitle">Своим величием он поразил немало туристов,
                        а внутри здание украшено еще лучше, чем снаружи.</div>
                </div>
                <div class="visit_block">
                    <div class="visit_block_img visit_block_img6"><img src="../assets/visit6.jpg" alt=""></div>
                    <div class="visit_block_title mr-25-15">Люди</div>
                    <div class="visit_block_subtitle">Несмотря на климат столицы, люди в городе очень добрые и всегда готовы прийти на помощь.</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "AstanaVisit"
    }
</script>

<style lang="less">
    .pad-x {
        padding: 130px 0;
    }
    .visit_wrap {
        display: flex;
        align-items: center;
    }
    .visit_wrap_blog {
        margin-right: 50px;
    }
    .visit_wrap_blog_title {
        font-weight: 600;
        font-size: 64px;
        line-height: 78px;
        letter-spacing: -0.03em;
        color: #000000;
    }
    .visit_wrap_blog_subtitle {
        font-weight: 400;
        font-size: 24px;
        line-height: 29px;
        letter-spacing: -0.03em;
        color: #444444;
    }
    .arr_right {
        font-weight: 500;
        font-size: 18px;
        line-height: 22px;
        letter-spacing: -0.03em;
        color: #03B0CD;
        padding-right: 120px;
        background-repeat: no-repeat;
        background-size: 110px;
        background-position-x: right;
        background-position-y: center;
        background-image: url(../assets/arrow-right.svg);
        transition: .3s all;
        &:hover {
            text-decoration: underline;
        }
    }
    .visit_wrapper {
        display: grid;
        grid-template-columns: repeat(3, 31%);
        grid-gap: 35px 45px;
        margin-top: 40px;
    }
    .visit_block_title {
        font-weight: 700;
        font-size: 18px;
        line-height: 22px;
        color: #000000;
    }
    .visit_block_subtitle {
        font-weight: 400;
        font-size: 14px;
        line-height: 23px;
        color: #444444;
    }
    .mr-25-15 {
        margin: 25px 0 15px 0;
    }
    .mr-15-25 {
        margin: 15px 0 25px 0;
    }
    .visit_block_img {
        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
    }
    .visit_block_img1 {
        width: 360px;
        height: 312px;
    }
    .visit_block_img2 {
        width: 360px;
        height: 213px;
    }
    .visit_block_img3 {
        width: 314px;
        height: 209px;
    }
    .visit_block_img4 {
        width: 360px;
        height: 180px;
    }
    .visit_block_img5 {
        width: 360px;
        height: 276px;
        margin-top: -60px;
    }
    .visit_block_img6 {
        width: 314px;
        height: 209px;
        margin-top: -50px;
    }
    /* media screen */
    @media screen and (max-width: 1500px) {
        .container {
            width: 1200px;
        }
        .visit_wrap_blog_title {
            font-size: 60px;
        }
        .visit_wrap_blog_subtitle {
            font-size: 22px;
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
        .visit_block_img1 {
            width: 320px;
            height: 290px;
        }
        .visit_block_title {
            font-size: 17px;
        }
        .visit_block_img2 {
            width: 330px;
            height: 200px;
        }
        .visit_block_img3 {
            width: 295px;
            height: 200px;
        }
        .visit_block_img4 {
            width: 325px;
            height: 160px;
        }
        .visit_block_img5 {
            width: 320px;
            height: 245px;
        }
        .visit_block_img6 {
            width: 300px;
            height: 200px;
        }
        .visit_wrap_blog_title {
            font-size: 52px;
            line-height: 48px;
        }
        .visit_wrap_blog_subtitle {
            font-size: 20px;
        }
        .arr_right {
            padding-right: 100px;
            background-size: 90px;
        }
    }

    @media screen and (max-width: 1100px) {
        .container {
            width: 900px;
        }
        .visit_wrapper {
            grid-template-columns: repeat(2, 47%);
        }
        .flex-direction {
            display: flex;
            flex-direction: column-reverse;
        }
        .order-0 {
            order: 0;
        }
        .order-1 {
            order: 1;
            margin: 25px 0 15px 0;
        }
        .order-2 {
            order: 2;
        }
        .mr-15-25 {
            margin: 0 0 0 0;
        }
        .visit_block_img5, .visit_block_img6 {
            margin-top: 0;
        }
        .visit_block_img {
            width: 100% !important;
            height: 370px;
            img {
                object-fit: cover;
            }
        }
        .visit_block_img1 {
            height: 370px;
        }
        .visit_wrap_blog_title {
            font-size: 48px;
        }
    }

    @media screen and (max-width: 1000px) {
        .container {
            width: 800px;
        }
        .visit_wrap_blog_title {
            font-size: 44px;
        }
    }

    @media screen and (max-width: 880px) {
        .container {
            width: 700px;
        }
        .visit_wrap_blog_title {
            font-size: 40px;
        }
        .visit_wrapper {
            grid-template-columns: 100%;
            grid-gap: 35px 0;
        }
        .visit_block_img {
            height: 300px;
        }
        .visit_block_img1 {
            height: 600px;
        }
    }

    @media screen and (max-width: 780px) {
        .container {
            width: 600px;
        }
        .visit_wrap_blog_title {
            font-size: 36px;
            line-height: 40px;
        }
        .visit_wrap_blog_subtitle {
            font-size: 18px;
        }
        .visit_block_img1 {
            height: 510px;
        }
    }

    @media screen and (max-width: 680px) {
        .container {
            width: 500px;
        }
        .visit_wrap_blog_title {
            font-size: 32px;
        }
        .arr_right {
            padding-right: 70px;
            background-size: 60px;
            font-size: 17px;
        }
        .visit_block_img1 {
            height: 430px;
        }
    }

    @media screen and (max-width: 570px) {
        .container {
            width: 100%;
            padding-left: 20px;
            padding-right: 20px;
        }
        .visit_wrap {
            flex-direction: column;
            align-items: baseline;
        }
    }

    @media screen and (max-width: 500px) {
        .visit_block_img {
            height: auto;
        }
    }

    @media screen and (max-width: 400px) {

    }
</style>
