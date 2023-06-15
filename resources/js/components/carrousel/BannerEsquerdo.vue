<template>
    <carousel :slides="slides" :interval="3000" controls indicators></carousel>
  </template>
  
  <script>
import Carousel from './Carousel.vue';
  export default {
    components: { Carousel},
    data: () => ({
      slides: [
        "./img/banner.jpg",
      ],
    }),
  };
  </script>
  
  <style></style>