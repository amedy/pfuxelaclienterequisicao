<template>
    <carousel :items-to-show="1.5">
        <slide v-for="slide in slides" :key="slide">
            <img src="https://picsum.photos/633/600?blur" alt="" />

        </slide>

        <template #addons>
            <navigation />
            <pagination />
        </template>
    </carousel>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
    props: ["slides"],
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data: () => ({
        slides: [
            "https://picsum.photos/633/600?blur",
            "https://picsum.photos/633/600?grayscale",
            "https://picsum.photos/633/600?blur",
            "https://picsum.photos/633/600",
            "/img/banner.jpg",
        ],
    }),
}
</script>

<style scoped>
.carousel {
    display: flex;
    justify-content: center;

}

.carrousel-iner {
    position: relative;
    width: 633px;

    overflow: hidden;
}
</style>
