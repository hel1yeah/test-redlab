<template>
  <carousel :per-page="1">
    <slide> Slide 1 Content </slide>
    <slide> Slide 2 Content </slide>
  </carousel>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  components: {
    Carousel,
    Slide,
  },
  mounted() {
    console.log(Carousel, 'asdfdsfsdfsdf')
  },
}
</script>
