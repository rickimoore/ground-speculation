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
                    <div class="upload--image"></div>
                    <h1>Upload</h1>
                </div>
            </div>
        </div>
        <div class="container">
            <vue-slider :railStyle="{backgroundColor: 'lightGrey'}" :processStyle="{backgroundColor: 'darkGrey'}" :dotStyle="{borderColor: 'grey'}" :max="100" v-model="value" />
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
            [require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'),
              require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'),
              require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'), require('../assets/Barcelona_Spain_0.png'), require('../assets/Como_Italy_0.png'), require('../assets/Dipperz_Germany_0.png'), require('../assets/Ditzum_Germany_0.png'), require('../assets/Douzy_France_0.png'),
              require('../assets/Eindhoven_Netherlands_A_0.png'), require('../assets/Eindhoven_Netherlands_B_0.png'), require('../assets/Eindhoven_Netherlands_C_0.png'), require('../assets/Fulda_Germany_0.png'), require('../assets/Houston_Texas_USA_0.png'), require('../assets/Liege_Belgium_0.png'),
              require('../assets/Montecarotto_Italien_0.png'), require('../assets/Mpumalonga_South-Africa_0.png'), require('../assets/Negev_Israel_0.png'), require('../assets/Paris_France_0.png'), require('../assets/Remiremont_France_0.png'),
            ],
            [require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'),
              require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'),
              require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'), require('../assets/Barcelona_Spain_1.png'), require('../assets/Como_Italy_1.png'), require('../assets/Dipperz_Germany_1.png'), require('../assets/Ditzum_Germany_1.png'), require('../assets/Douzy_France_1.png'),
              require('../assets/Eindhoven_Netherlands_A_1.png'), require('../assets/Eindhoven_Netherlands_B_1.png'), require('../assets/Eindhoven_Netherlands_C_1.png'), require('../assets/Fulda_Germany_1.png'), require('../assets/Houston_Texas_USA_1.png'), require('../assets/Liege_Belgium_1.png'),
              require('../assets/Montecarotto_Italien_1.png'), require('../assets/Mpumalonga_South-Africa_1.png'), require('../assets/Negev_Israel_1.png'), require('../assets/Paris_France_1.png'), require('../assets/Remiremont_France_1.png'),
            ],
            [require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'),
              require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'),
              require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'), require('../assets/Barcelona_Spain_2.png'), require('../assets/Como_Italy_2.png'), require('../assets/Dipperz_Germany_2.png'), require('../assets/Ditzum_Germany_2.png'), require('../assets/Douzy_France_2.png'),
              require('../assets/Eindhoven_Netherlands_A_2.png'), require('../assets/Eindhoven_Netherlands_B_2.png'), require('../assets/Eindhoven_Netherlands_C_2.png'), require('../assets/Fulda_Germany_2.png'), require('../assets/Houston_Texas_USA_2.png'), require('../assets/Liege_Belgium_2.png'),
              require('../assets/Montecarotto_Italien_2.png'), require('../assets/Mpumalonga_South-Africa_2.png'), require('../assets/Negev_Israel_2.png'), require('../assets/Paris_France_2.png'), require('../assets/Remiremont_France_2.png'),
            ],
            [require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'),
              require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'),
              require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'), require('../assets/Barcelona_Spain_3.png'), require('../assets/Como_Italy_3.png'), require('../assets/Dipperz_Germany_3.png'), require('../assets/Ditzum_Germany_3.png'), require('../assets/Douzy_France_3.png'),
              require('../assets/Eindhoven_Netherlands_A_3.png'), require('../assets/Eindhoven_Netherlands_B_3.png'), require('../assets/Eindhoven_Netherlands_C_3.png'), require('../assets/Fulda_Germany_3.png'), require('../assets/Houston_Texas_USA_3.png'), require('../assets/Liege_Belgium_3.png'),
              require('../assets/Montecarotto_Italien_3.png'), require('../assets/Mpumalonga_South-Africa_3.png'), require('../assets/Negev_Israel_3.png'), require('../assets/Paris_France_3.png'), require('../assets/Remiremont_France_3.png'),
            ],
            [require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'),
              require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'),
              require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'), require('../assets/Barcelona_Spain_4.png'), require('../assets/Como_Italy_4.png'), require('../assets/Dipperz_Germany_4.png'), require('../assets/Ditzum_Germany_4.png'), require('../assets/Douzy_France_4.png'),
              require('../assets/Eindhoven_Netherlands_A_4.png'), require('../assets/Eindhoven_Netherlands_B_4.png'), require('../assets/Eindhoven_Netherlands_C_4.png'), require('../assets/Fulda_Germany_4.png'), require('../assets/Houston_Texas_USA_4.png'), require('../assets/Liege_Belgium_4.png'),
              require('../assets/Montecarotto_Italien_4.png'), require('../assets/Mpumalonga_South-Africa_4.png'), require('../assets/Negev_Israel_3.png'), require('../assets/Paris_France_4.png'), require('../assets/Remiremont_France_4.png'),
            ],
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
        width: 60px;
    }
    .chroma--upload {
        width: 600px;
        height: 100%;
        background-color: white;
        position: absolute;
        right: -650px;
        top: 0;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }
    .upload--image {
        background-image: url("../assets/circle_upload.png");
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        width: 80%;
        height: 80%;
        position: absolute;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        cursor: pointer;
    }
</style>