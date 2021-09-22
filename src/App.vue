<template>
  <section-home></section-home>
  <section-cards></section-cards>
  <section-cleaning></section-cleaning>
  <test></test>
</template>

<script>
import SectionHome from '@/views/SectionHome.vue'
import SectionCards from '@/views/SectionCards.vue'
import SectionCleaning from '@/views/SectionCleaning.vue'
import Test from './views/test.vue'

export default {
  components: {
    SectionHome,
    SectionCards,
    SectionCleaning,
    Test,
  },
}
</script>

<style></style>
