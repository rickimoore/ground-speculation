<template>
    <div class="page">
        <div class="container">
            <div class="window" :style="'width: ' + this.window + 'px; margin-left: -' + this.value + '%'">
                <div v-for="row in rows" class="row">
                    <div v-for="item in row" class="block">
                        <img class="slide_image" alt="image" :src="item">
                    </div>
                </div>
                <div class="chroma--upload">
                    <h1>Upload</h1>
                </div>
            </div>
        </div>
        <div class="container">
            <vue-slider :max="100" v-model="value" />
        </div>
    </div>
</template>
<script>
  import VueSlider from 'vue-slider-component'
  import 'vue-slider-component/theme/antd.css'
    export default {
      name: 'Archive',
      components: {
        VueSlider
      },
      data: () => {
        return {
          window: null,
          value: 0,
          rows: [
            [require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png')],
            [require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png')],
            [require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png')],
            [require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png')],
            [require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png')],
          ]
        }
      },
      mounted(){
        this.window = (window.outerWidth * 1.5) - 300;
      }
    }
</script>
<style scoped>
    .page {
        align-items: center;
        padding: 0 100px;
        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
    }
    .row {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
    }
    .container {
        width: 100%;
        overflow: hidden;
    }
    .window {
        position: relative;
        height: 500px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        float: left;
    }
    .block {
        height: 80px;
        width: 80px;
        margin: 10px;
    }
    .slide_image{
        width: 80px;
    }
    .chroma--upload {
        width: 600px;
        height: 100%;
        background-color: white;
        position: absolute;
        right: -600px;
        top: 0;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }
</style>