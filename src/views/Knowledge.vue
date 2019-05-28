<template>
    <div class="page">
        <carousel :perPage="1" :navigationEnabled="false" :paginationEnabled="false" style="width: 100%; margin-top: 100px">
            <slide v-for="slide in slideShow">
                <div class="slide--content">
                    <div class="slide--image">
                        <div class="slide--title off-slide">
                            <p>{{slide.title}}</p>
                        </div>
                        <img  v-if="isOverlay" class="slide_overlay" alt="ground image" src="../assets/Dipperz_Germany_0.png">
                        <img class="slide_image" alt="ground image" :src="slide.image">
                        <div class="slide--data off-slide">
                            <p class="slide--data-text">{{slide.text}}</p>
                        </div>
                    </div>
                </div>
            </slide>
        </carousel>
        <div class="slide--controls">
            <div class="toggle">
                <p class="option"
                   v-on:click="isOverlay = true"
                   v-bind:class="{ active: isOverlay }">On</p>
                <span>/</span>
                <p class="option"
                   v-on:click="isOverlay = false"
                   v-bind:class="{ active: !isOverlay }">Off</p>
            </div>
        </div>
    </div>
</template>
<script>
  import { Carousel, Slide } from 'vue-carousel';
    export default {
      name: 'knowledge',
      components: {
        Carousel,
        Slide
      },
      data: () => {
        return {
          isOverlay: false,
          slideShow: [
            {
              title: 'Color',
              image: require('../assets/color_placeholder.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore ' +
              'et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex '
            },
            {
              title: 'Width',
              image: require('../assets/width_placeholder.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore ' +
              'et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex '
            },
            {
              title: 'Pattern',
              image: require('../assets/pattern_placeholder.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore ' +
              'et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex '
            }
          ]
        }
      }
    }
</script>
<style scoped>
    .page {
        background-color: #1E1E1E;
        color: white;
    }
    .slide--content {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        position: relative;
    }
    .off-slide {
        position: absolute;
        height: 100%;
        top: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .slide--title {
        left: 20%;
    }
    .slide--data{
        right: 4%;
        width: 350px;
    }
    .slide--data-text{
        text-align: left;
    }
    .slide_image{
        width: 40%;
        position: relative;
        z-index: 99;
        pointer-events: none;
    }
    .slide_overlay {
        width: 40%;
        position: absolute;
        left: 50%;
        margin-left: -20%;
        opacity: .6;
        top: 0;
        pointer-events: none;
    }
    .slide--controls {
        width: 200px;
        position: relative;
        z-index: 999;
    }
    .toggle {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }
    .option {
        padding: 10px;
        cursor: pointer;
    }
    .VueCarousel-navigation button {
        background-color: red;
    }
    .active {
        text-decoration: underline;
    }
</style>