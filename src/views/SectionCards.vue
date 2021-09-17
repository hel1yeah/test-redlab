<template>
  <section class="cards">
    <div class="container">
      <div class="cards--inner">
        <div class="card" v-for="card in cards" :key="card">
          <div class="card__article-text">{{ card.article }}</div>
          <div class="card__text">{{ card.text }}</div>
          <img class="card__text-img" :src="card.img" :alt="card.text" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          text: 'Тщательно отобранный персонал',
          img: require('./../assets/images/1card.png'),
          article:
            '1Не нужно тратить время, силы и ресурсы на разме- щение вакансий, проведе- ние собеседований, про- верку кандидатов на должность уборщицы. За счет больших объемов мы можем сделать это эффективнее.',
        },
        {
          text: 'Качественная эко-химия',
          img: require('./../assets/images/2card.png'),
          article:
            '2Не нужно тратить время, силы и ресурсы на разме- щение вакансий, проведе- ние собеседований, про- верку кандидатов на должность уборщицы. За счет больших объемов мы можем сделать это эффективнее.',
        },
        {
          text: 'Контролируем качество',
          img: require('./../assets/images/3card.png'),
          article:
            '3Не нужно тратить время, силы и ресурсы на разме- щение вакансий, проведе- ние собеседований, про- верку кандидатов на должность уборщицы. За счет больших объемов мы можем сделать это эффективнее.',
        },
        {
          text: 'Работаем круглосуточно',
          img: require('./../assets/images/4card.png'),
          article:
            '4Не нужно тратить время, силы и ресурсы на разме- щение вакансий, проведе- ние собеседований, про- верку кандидатов на должность уборщицы. За счет больших объемов мы можем сделать это эффективнее.',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/_mixin.scss';

.cards {
  margin: 73px 0 0 0;
}

.cards--inner {
  @include myFlex;
}

.card {
  border-radius: 8px;
  background-color: $light-grey;
  width: 300px;

  height: 328px;

  text-align: center;
  @include myFlex;
  flex-direction: column;
  position: relative;
  overflow: hidden;
}
.card__article-text {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: $purple-color;
  padding: 30px;
  color: $primary-color;
  text-align: left;
  font-size: 16px;
  line-height: 140%;
  font-weight: 400;
}
.card__text {
  margin-top: 20px;
  font-family: 'TTTravels-Medium', sans-serif;
  line-height: 130%;
  max-width: 170px;
}
.card__text-img {
}
</style>
