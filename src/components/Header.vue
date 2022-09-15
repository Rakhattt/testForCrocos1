<template>
    <header :class="{header_color: scrollPosition > 100}">
      <div class="container_head">
        <a href="/" class="logo">
          <img src="../assets/logo.svg" alt="">
        </a>
        <ul class="header_ul dn">
          <li><a href="javascript:;">Tourism</a></li>
          <li><a href="javascript:;">Invest</a></li>
          <li><a href="javascript:;">Convention bureau</a></li>
        </ul>
        <div class="df">
          <div class="social_icons mr-7">
            <a href="javascript:;" class="instagram"></a>
            <a href="javascript:;" class="youtube"></a>
            <a href="javascript:;" class="facebook"></a>
          </div >
          <div class="search_pos mr-7">
            <div @click="height = !height" class="magnifyingGlass"></div>
            <form class="search" v-if="height" :class="{'search_active': height}">
              <input type="search" placeholder="поиск">
              <span @click="height = !height"></span>
            </form>
          </div>
          <div class="menu__icon mr-7"  @click="showMenu = !showMenu">
            <span></span>
          </div>
          <div class="under_nav" v-if="showMenu">
            <ul class="header_ul">
              <li><a href="javascript:;">Tourism</a></li>
              <li><a href="javascript:;">Invest</a></li>
              <li><a href="javascript:;">Convention bureau</a></li>
            </ul>
          </div>
          <div class="lang_block">
            <div class="lang_choice" @click="show = !show">
              <span>Ru</span>
            </div>
            <div class="other_lang" v-if="show">
              <a href="javascript:;">En</a>
              <a href="javascript:;" class="active">Ru</a>
              <a href="javascript:;">Kz</a>
            </div>
          </div>
        </div>
        <div class="basket">
            <div class="basket_title">Корзина</div>
            <div class="basket_subtitle">0 тг.</div>
          </div>
      </div>
    </header>
</template>

<script>
  export default {
    name: 'Header',
    data() {
      return {
        height: false,
        show: false,
        scrollPosition: null,
        showMenu: false
      }
    },
    methods: {
      updateScroll() {
        this.scrollPosition = window.scrollY
      }
    },
    mounted() {
      window.addEventListener('scroll', this.updateScroll);
    }
  }
</script>


<style lang="less">
  .under_nav {
    position: absolute;
    right: 0%;
    top: 139%;
    padding: 20px 10px;
    width: 250px;
    max-height: 350px;
    overflow: auto;
    z-index: 5;
    box-shadow: 0 3px 9px #000000;
    color: #0F2533;
    background-color: #011832c4;
  }
  .header_color {
    background-color: #011832c4;
  }
  header {
    padding: 20px 0;
    background-color: rgba(1, 24, 50, 0.3);
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
    z-index: 90;
    -webkit-transition: 0.6s;
    transition: 0.6s;
  }
  .container_head {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    width: 1500px;
    margin: 0 auto;
    position: relative;
  }
  .logo {
    width: 140px;
    height: 40px;
    img {
      display: block;
      width: 100%;
      height: 100%;
      object-fit: contain;
      flex-shrink: 0;
    }
  }
  .header_ul {
    display: flex;
    justify-content: center;
    align-items: center;
    li:not(:last-child) {
      margin-right: 55px;
    }
    li a {
      font-weight: 500;
      font-size: 16px;
      line-height: 20px;
      text-transform: uppercase;
      color: #FFFFFF;
      padding: 6px 18px;
      border-radius: 30px;
      &:hover {
        background-color: #fff;
        color: #011832;
      }
    }
  }
  .social_icons {
    display: flex;
    justify-content: center;
    align-items: center;
    a {
      width: 20px;
      height: 20px;
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center;
      transition: .3s;
    }
    a:not(:last-child) {
      margin-right: 27px;
    }
    .instagram {
      background-image: url(../assets/insta.svg);
      &:hover {
        background-image: url(../assets/insta_hover.svg);
      }
    }
    .youtube {
      background-image: url(../assets/youtube.svg);
      &:hover {
        background-image: url(../assets/youtube_hover.svg);
      }
    }
    .facebook {
      background-image: url(../assets/facebook.svg);
      &:hover {
        background-image: url(../assets/facebook_hover.svg);
      }
    }
  }
  .magnifyingGlass {
    width: 25px;
    height: 25px;
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
    cursor: pointer;
    background-image: url(../assets/magnifyingGlass.svg);
  }
  .lang_choice {
    cursor: pointer;
    padding-right: 17px;
    background: url(../assets/ar_down.svg) right center / 12px no-repeat;
    span {
      font-weight: 500;
      font-size: 16px;
      line-height: 20px;
      color: #FFFFFF;
      text-transform: uppercase;
    }
  }
  .basket {
    padding-left: 35px;
    background: url(../assets/shopping.svg) left center / 27px no-repeat;
    .basket_title {
      font-weight: 500;
      font-size: 16px;
      line-height: 20px;
      color: #FFFFFF;
    }
    .basket_subtitle {
      font-weight: 500;
      font-size: 9px;
      line-height: 11px;
      text-transform: uppercase;
      color: #FFFFFF;
    }
  }
  .df {
    display: flex;
    justify-content: space-between;
    align-items: center;
    /*div:not(:last-child) {*/
    /*  margin-right: 59px;*/
    /*}*/
  }
  .mr-7 {
    margin-right: 59px;
  }
  .search_pos {
    position: relative;
  }
  .search_active {
    height: 40px !important;
  }
  .search {
    position: absolute;
    right: 0%;
    height: 0px;
    overflow: hidden;
    top: 53px;
    box-shadow: 0px 4px 8px rgb(34 0 34 / 16%);
    transition: 0.6s;
    z-index: 1;
    input {
      width: 170px;
      padding: 10px 20px;
      font-size: 14px;
      border: 1px solid #011832;
      outline: none;
    }
    span {
      position: absolute;
      right: 20px;
      top: 6px;
      width: 20px;
      height: 20px;
      opacity: 0.3;
      cursor: pointer;
      &:hover {
        opacity: 1;
      }
      &:before, &:after {
        position: absolute;
        left: 15px;
        content: ' ';
        height: 25px;
        width: 2px;
        background-color: #333;
      }
      &:before {
        transform: rotate(45deg);
      }
      &:after {
        transform: rotate(-45deg);
      }
    }
  }
  .lang_block {
    position: relative;
    .other_lang {
      position: absolute;
      left: 0;
      right: 0;
      z-index: 2;
      top: 100%;
      overflow: hidden;
      border-radius: 5px;
      margin-top: 3px;
      a.active {
        color: #011832;
        background-color: #fff;
      }
      a {
        color: #fff;
        font-size: 16px;
        font-weight: normal;
        padding: 7px 10px;
        background-color: #011832;
        display: block;
        transition: 0.3s;
        &:hover {
          background-color: #fff;
          color: #011832;
        }
      }
    }
  }
  .other_lang, .search_active, .under_nav {
    transform: translateY(-150%);
    animation: ani .8s forwards;
  }
  @keyframes ani {
    0% {transform: translateY(-15%);}
    100% {transform: translateY(0);}
  }
  .menu__icon {
    display: block;
    z-index: 5;
    cursor: pointer;
    position: relative;
    width: 30px;
    height: 18px;
  }
  .menu__icon span,
  .menu__icon::before,
  .menu__icon::after {
    position: absolute;
    right: 0;
    height: 10%;
    -webkit-transition: all 0.3s ease 0s;
    transition: all 0.3s ease 0s;
    background-color: #FFFFFF;
  }
  .menu__icon::before,
  .menu__icon::after {
    content: "";
  }
  .menu__icon::before {
    top: 0;
    width: 70%;
  }
  .menu__icon::after {
    bottom: 0;
    width: 40%;
  }
  .menu__icon span {
    top: 50%;
    -webkit-transform: scale(1) translate(0, -50%);
    transform: scale(1) translate(0, -50%);
    width: 100%;
  }
  .menu__icon.active span {
    -webkit-transform: scale(0) translate(0, -50%);
    transform: scale(0) translate(0, -50%);
  }
  .menu__icon.active::before {
    top: 50%;
    -webkit-transform: rotate(-45deg) translate(0px, -50%);
    transform: rotate(-45deg) translate(0px, -50%);
  }
  .menu__icon.active::after {
    bottom: 50%;
    -webkit-transform: rotate(45deg) translate(0px, 50%);
    transform: rotate(45deg) translate(0px, 50%);
  }
  /* media screen */
  @media screen and (max-width: 1600px) {
    .container_head {
      width: 1300px;
    }
    .basket {
      display: none;
    }
    header {
      padding: 15px 0;
    }
    .header_ul li:not(:last-child) {
      margin-right: 35px;
    }
    .mr-7 {
      margin-right: 40px;
    }
    .search {
      top: 47px;
    }
  }

  @media screen and (max-width: 1500px) {
    .container_head {
      width: 1200px;
    }

  }

  @media screen and (max-width: 1350px) {
    .container_head {
      width: 1100px;
    }
  }

  @media screen and (max-width: 1200px) {
    .container_head {
      width: 1000px;
    }
    .header_ul li:not(:last-child) {
      margin-right: 20px;
    }
    .header_ul li a {
      font-size: 15px;
    }
    .social_icons a:not(:last-child) {
      margin-right: 15px;
    }
    .mr-7 {
      margin-right: 30px;
    }
  }

  @media screen and (max-width: 1100px) {
    .container_head {
      width: 900px;
    }
    .social_icons {
      display: none;
    }
  }

  @media screen and (max-width: 1000px) {
    .container_head {
      width: 800px;
    }
    .dn {
      display: none;
    }
    .header_ul {
      align-items: baseline;
      flex-direction: column;
    }
    .header_ul li:not(:last-child) {
      margin-right: 0;
      margin-bottom: 15px;
    }
    .lang_block {
      order: 1;
    }
    .menu__icon {
      order: 2;
    }
    .mr-7 {
      margin-right: 0;
    }
    .lang_block {
      margin: 0 20px;
    }
  }

  @media screen and (max-width: 880px) {
    .container_head {
      width: 700px;
    }
  }

  @media screen and (max-width: 780px) {
    .container_head {
      width: 600px;
    }
  }

  @media screen and (max-width: 680px) {
    .container_head {
      width: 500px;
    }
  }

  @media screen and (max-width: 570px) {
    .container_head {
      width: 100%;
      padding-left: 20px;
      padding-right: 20px;
    }
  }

  @media screen and (max-width: 500px) {

  }

  @media screen and (max-width: 400px) {
    .lang_choice span {
      font-size: 15px;
    }
    .lang_block {
      margin: 0px 15px;
    }
  }

</style>
