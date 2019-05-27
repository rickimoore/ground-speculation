<template>
  <div class="page">
    <div class="full_map" :style="{'background-image': 'url(' + require('../assets/world-map.png') + ')'}">
    </div>
  </div>
</template>

<style scoped>
  .full_map{
    height: 80%;
    width: 80%;
    background-size: 100% auto;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
