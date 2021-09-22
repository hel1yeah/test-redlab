<template>
  <section class="cleaning">
    <div class="cleaning__wrapper">
      <div class="cleaning__text">
        <h2 class="cleaning__title">Как мы убераем</h2>
        <p class="cleaning__descr">
          Клинер приезжает в назначенное время со всем необходимым и сразу
          приступает к делу. Вам остаётся только оценить результат.
        </p>
      </div>
    </div>
    <div class="cleaning__gallery">
      <div class="cleaning__menu-container">
        <span class="cleaning__menu-descr">Как мы убераем</span>
        <ul class="cleaning__menu">
          <li class="cleaning__menu-item">Кухня</li>
          <li class="cleaning__menu-item">Комнаты</li>
          <li class="cleaning__menu-item">Ванная</li>
          <li class="cleaning__menu-item">Прихожая</li>
        </ul>
      </div>
      <img
        class="cleaning__img"
        src="./../assets/images/cleaning1.jpg"
        alt="kitchen"
      />
    </div>
  </section>
</template>

<script>
import { gsap } from 'gsap'

import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

export default {
  name: 'SectionCleaning',
  data() {
    return {}
  },
  mounted() {
    this.gsapTitleFrom()
    this.gsapGallery()
  },
  methods: {
    gsapTitleFrom() {
      let tl = gsap.timeline({
        scrollTrigger: {
          trigger: '.cleaning__title',
          start: 'top bottom',
          toggleActions: 'play none none none',
        },
      })
      tl.from('.cleaning__title', {
        y: 120,
        opacity: 0,
        duration: 1.5,
        ease: 'power3.inOutinOut',
      })
      tl.from(
        '.cleaning__descr',
        {
          y: 120,
          opacity: 0,
          duration: 1.5,
          ease: 'power3.inOutinOut',
        },
        '-=1'
      )
    },

    gsapGallery() {
      let tl = gsap.timeline({
        scrollTrigger: {
          trigger: '.cleaning__gallery',
          start: 'bottom bottom+=100',
        },
      })
      tl.fromTo(
        '.cleaning__img',
        {
          duration: 2,
          height: '80%',
          width: '56%',
        },
        {
          right: '0%',
          transform: 'translateX(0%)',
          borderRadius: '0px',
          height: '100%',
          width: '77%',
        }
      )

      tl.fromTo(
        '.cleaning__menu-container',
        {
          x: '-100%',
          y: '-200px',
          opacity: 0,
          duration: 1.5,
          ease: 'power3.inOutinOut',
        },
        { x: '0%', y: '0px', opacity: 1 }
      )
    },
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/_mixin.scss';
.cleaning {
  margin-top: 150px;
}
.cleaning__wrapper {
  max-width: 1094px;
  max-height: 630px;
  margin: 0 auto;
}
.cleaning__text {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  font-family: 'TTTravels-Regular', sans-serif;
  margin: 0 0 52px 0;
}
.cleaning__title {
  font-size: 44px;
  line-height: 120%;
}
.cleaning__descr {
  font-size: 18px;
  line-height: 140%;
  max-width: 414px;
}
.cleaning__gallery {
  overflow: hidden;
  position: relative;
  height: 100vh;
}
.cleaning__img {
  border-radius: 8px;
  overflow: hidden;
  display: block;
  position: absolute;
  height: 100%;
  width: 77%;
  top: 0;
  right: 50%;
  transform: translateX(50%);
  z-index: 0;
}

.cleaning__menu-container {
  z-index: 1;
  position: absolute;
  top: 0;
  left: 0;
  width: 23%;
  height: 100%;
  background-color: $purple-color;
  color: $primary-color;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.cleaning__menu-descr {
  position: absolute;
  top: 35px;
  left: 53px;

  font-family: 'TTTravels-Medium', sans-serif;
  font-weight: 500;
  font-size: 16px;
  line-height: 130%;
}
.cleaning__menu {
  height: 278px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-direction: column;
}
.cleaning__menu-item {
  list-style-type: none;
  opacity: 0.7;
  font-size: 44px;
  line-height: 120%;
  font-family: 'TTTravels-Regular', sans-serif;
}
</style>
