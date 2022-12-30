<template>
  <header :class="{ 'header__active': isHeaderActive }">
    <div class="wrapper">
    <div class="header__wrapper">
      <div class="header__logo">
        <nuxt-link to="/">
          <img class="header__logo-img"
               src="../public/img/header-logo.svg" alt="navbar-title"/>
        </nuxt-link>
      </div>
      <nav class="navbar">
        <ul class="nav__list">
          <li class="nav__item">
            <a class="nav__link" href="#">Главная</a>
          </li>
          <li class="nav__item">
            <a class="nav__link" href="#">Обо мне</a>
          </li>
          <li class="nav__item">
            <a class="nav__link" href="#">Магазин</a>
          </li>
          <li class="nav__item">
            <a class="nav__link" href="#">Где купить</a>
          </li>
        </ul>
      </nav>
      <div class="header__cart">
          <img class="header__cart-img" src="../public/img/header-cart.svg" width="30" height="34" alt="1">
          <use xlink:href="#cart-icon"></use>
          <text class="cart-counter">{{ counter }}</text>
      </div>
    </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      isHeaderActive: false,
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset > 50) {
        this.isHeaderActive = true;
      } else {
        this.isHeaderActive = false;
      }
    },
  },
};
</script>

<style>
.wrapper {
  margin: 0 auto;
  padding: 20px;
}
/*.header__active {*/
/*  background: white;*/
/*}*/
header{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  transition: all 0.2s linear;
  padding-bottom: 20px;
  z-index: 11;
  background: white;
}

header.fixed {
  top: -100px;
}

.header__wrapper {
  display: flex;
  align-content: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 30px 260px 0 260px;
}

.nav__list {
  list-style: none;
  margin: 0;
  padding-left: 300px;
  display: flex;
  align-items: center;
}

.nav__item {
  padding: 0 15px;
}

.nav__link{
  color: #2F2E2E;
  text-decoration: none;
  font-size: 16px;
}

.header__logo-img {
  width: 172px;
  height: 37px;
}
.cart-counter {
  font-size: 12px;
  fill: white;
}
.header__cart{
  display: flex;
  align-items: end;
  justify-content: end;
}

.header__cart-img{
  position: absolute;
}

text{
  position: relative;
  color: white;
  left: 12px;
  top: 7px;
}
@media (max-width: 767px) {
  header {
    padding: 10px;
  }
}
</style>