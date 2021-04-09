<template>
  <Carousel3d>
    <div v-for="index of 5" :key="index">
      <slide :index="index - 1">
        <img src="@/assets/static/img/slide2.jpg" alt="alt"
      /></slide>
    </div>
  </Carousel3d>
</template>

<script>
import { Carousel3d, Slide } from "vue-carousel-3d";

export default {
  name: "CaruselComponent",
  components: {
    Carousel3d,
    Slide,
  },
  data() {
    return {};
  },
};
</script>
