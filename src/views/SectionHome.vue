<template>
  <section class="home">
    <app-header> </app-header>
    <div class="home-inner">
      <div class="home__img"></div>
      <div class="home__text">
        <h1 class="home__text-title">Уборка квартир в Киеве</h1>
        <p class="home__text-descr">
          Мы уберем у вас дома или в офисе. Наведем чистоту после ремонта и
          проведем генеральную уборку.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
export default {
  components: {
    AppHeader,
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/_mixin.scss';
.home {
  position: relative;
}
.home-inner {
  @include myFlex;
}
.home__img {
  background-image: url('./../assets/images/header-img.jpg');
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  box-sizing: content-box;
  width: 100%;
  flex-shrink: 1;
  height: 100vh;
}
.home__text {
  box-sizing: content-box;
  flex-shrink: 1;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.home__text-title {
  max-width: 380px;
  font-size: 76px;
  line-height: 110%;
  font-family: 'TTTravels-Regular', sans-serif;
  font-weight: normal;
}
.home__text-descr {
  width: 380px;
  font-weight: normal;
  font-size: 18px;
  line-height: 140%;
  font-family: 'TTTravels-Regular', sans-serif;
}
</style>
