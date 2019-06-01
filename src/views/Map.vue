<template>
  <div class="page">
    <div v-if="!isClimaticMap" class="full_map" :style="{'background-image': 'url(' + require('../assets/outline-map.png') + ')'}" />
    <div v-if="isClimaticMap" class="full_map" :style="{'background-image': 'url(' + require('../assets/climatic-map.png') + ')'}" />
    <div class="slide--controls">
      <div class="toggle">
        <p class="option"
           v-on:click="isClimaticMap = true"
           v-bind:class="{ active: isClimaticMap }">On</p>
        <span>/</span>
        <p class="option"
           v-on:click="isClimaticMap = false"
           v-bind:class="{ active: !isClimaticMap }">Off</p>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'global',
    data: () => {
      return {
        isClimaticMap: false
      }
    }
  }
</script>
<style scoped>
  .full_map{
    height: 80%;
    width: 80%;
    background-size: 100% auto;
    background-repeat: no-repeat;
    background-position: center;
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
  .active {
    text-decoration: underline;
  }
</style>
