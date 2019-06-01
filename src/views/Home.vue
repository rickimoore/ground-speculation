<template>
  <div class="home">
    <img v-on:click="viewManifesto()" v-if="!isManifesto"
        class="placeholder" alt="Vue logo"
        src="../assets/chromas_start.gif">
    <div v-if="isManifesto">
      <div v-for="(sentence, index) in texts" v-bind:key="index">
        <p v-bind:key="index2" class="monologue" v-for="(text, index2) in sentence">{{text}}</p>
      </div>
      <router-link to="/map">
        <img class="next-logo" src="../assets/arrow.png">
      </router-link>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  data: () => {
    return {
      isManifesto: false,
      texts: [
        ['soil', 'is a heritable right ', 'to all mankind.'],
        ['It must not be', 'a commodity, nor ', 'object of', 'speculation.'],
        ['It is owned by', 'no one and shared', 'by everyone.'],
        ['Soil', 'is unappropriatable.', 'it is a collective good.'],
        ['All soils are free', 'and must be', 'separated from the owned ground.'],
        ['The property right', 'of soil becomes ', 'a use right.'],
        ['Soil', 'must be restored.'],
        ['The suitability of', 'a soil determines', 'its use.'],
        ['By transplanting', 'soils, this suitability is adapted.']
      ]
    }
  },
  methods: {
    viewManifesto: function () {
      this.isManifesto = true
    }
  }
}
</script>
<style scoped>
  .home {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .placeholder {
    width: 50%
  }
  .monologue {
    font-family: Adobe Garamond Pro, sans-serif;
  }
  .next-logo{
    width: 50px;
  }
</style>
