<template>
    <div class="page">
        <carousel :perPage="1" style="width: 100%">
            <slide v-for="slide in slideShow">
                <img class="slide_image" alt="ground image" :src="slide">
            </slide>
        </carousel>
    </div>
</template>
<script>
  import { Carousel, Slide } from 'vue-carousel';
    export default {
      components: {
        Carousel,
        Slide
      },
      data: () => {
        return {
          slideShow: [
            require('../assets/chromas.gif'),
            require('../assets/topview-footage-1.png'),
            require('../assets/topview-footage-2.png'),
            require('../assets/topview-footage-3.png')
          ]
        }
      }
    }

</script>
<style scoped>
    .slide_image {
        width: 700px
    }
</style>