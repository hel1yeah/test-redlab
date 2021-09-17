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

      <img
        class="cleaning__img"
        src="./../assets/images/cleaning1.jpg"
        alt="kitchen"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionCleaning',
  data() {
    return {}
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
.cleaning__img {
  border-radius: 8px;
  overflow: hidden;
  max-width: 1094px;
  max-height: 630px;
}
</style>
