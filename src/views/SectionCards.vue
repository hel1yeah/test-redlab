<template>
    <section class="cards">
        <div class="container">
            <div class="cards--inner">
                <div class="card" v-for="card in cards" :key="card">
                    <div class="card__text">{{ card.text }}</div>
                    <img
                        class="card__text-img"
                        :src="card.img"
                        :alt="card.text"
                    />
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
                },
                {
                    text: 'Качественная эко-химия',
                    img: require('./../assets/images/2card.png'),
                },
                {
                    text: 'Контролируем качество',
                    img: require('./../assets/images/3card.png'),
                },
                {
                    text: 'Работаем круглосуточно',
                    img: require('./../assets/images/4card.png'),
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
    max-width: 300px;
    height: 328px;
    max-height: 328px;
    text-align: center;

    @include myFlex;
    flex-direction: column;
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
