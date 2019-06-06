<template>
    <div class="page">
        <carousel :perPage="1" :navigationEnabled="false" :paginationEnabled="false" style="width: 100%; margin-top: 100px">
            <slide v-for="slide in slideShow">
                <div class="slide--content">
                    <div class="slide--image">
                        <div class="slide--title off-slide">
                            <p class="slide--sub-title">{{slide.title}}</p>
                        </div>
                        <img  v-if="isOverlay" class="slide_overlay" alt="ground image" src="../assets/Dipperz_Germany_0.png">
                        <img class="slide_image" alt="ground image" :src="slide.image">
                        <div class="slide--data off-slide">
                            <h3 v-if="slide.subTitle" class="slide--sub-title">{{slide.subTitle}}</h3>
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
      name: 'participate',
      components: {
        Carousel,
        Slide
      },
      data: () => {
        return {
          isOverlay: false,
          slideShow: [
            {
              title: 'Size Ratio',
              image: require('../assets/tool_ratio1.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'The wideness of the zones should be in ratio with each other at a balanced soil. If one zone is small or narrow and the other one is wide or large, then the chroma, and thus the soil is out of balance. A chroma with a good spreading of the zones is an indication of a balanced soil.'
            },
            {
              title: 'Color',
              subTitle: 'General Soil Fertility',
              image: require('../assets/tool_color.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Looking at the colour of the central zone, the general fertility of the soil can be evaluated. A fairly white zone speaks for a very fertile soil, a creamy to light beige coloured zone references an average fertility. If the zone is rather dark, this could point out a chemically threatened soil.'
            },
            {
              title: 'Color',
              image: require('../assets/tool_color2.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Desirable colours for the inner and intermediate zone range from cream, light brown, beige to orange and red. Those colours refer to a healthy soil, whereas dark, ash colours or violet tones reveal a disturbance in the soil.'
            },
            {
              title: 'Color',
              subTitle: 'Condition of humus',
              image: require('../assets/tool_color3.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'If the external zone displays a dark brown , closed edge, the soil contains raw or burned organic matter. Stable humus is indicated by a light brown, beige colour in the shape of small clouds sitting on top of the formed prickles.'
            },
            {
              title: 'Pattern',
              subTitle: 'quality of soil life',
              image: require('../assets/tool_pattern.png'),
              overlay: require('../assets/placeholder-chroma.png'),
              text: 'Besides colour and size, the formed edge of the intermediate zone also reveals information about the status of life within the soil. If it is evenly covered with prickles, the soil microorganisms are active. The more vibrant and dynamic this pattern is taking shape, the more activity can be found in the soil.'
            }
          ]
        }
      }
    }
</script>
<style scoped>
    .page {
        background-color: #1A1818;
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
        width: 43%;
        position: absolute;
        left: 50%;
        margin-left: -21%;
        opacity: .9;
        top: -5%;
        pointer-events: none;
    }
    .slide--controls {
        width: 200px;
        position: relative;
        z-index: 999;
    }
    .slide--sub-title{
        text-align: left;
        width: 100%;
        text-transform: uppercase;
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
    h3 {
        font-family: 'TheSans', sans-serif;
    }
</style>