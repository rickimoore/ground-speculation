<template>
    <div class="nav">
        <div class="nav_bar top_nav">
            <div class="link">
                <router-link class="router-link" to="/map">
                    <p v-bind:class="{ dark: isDark }">Global</p>
                </router-link>
            </div>
            <div class="logo">
                <router-link class="router-link" to="/">
                    <img v-if="!isDark" class="nav_logo" alt="Vue logo" src="../assets/logo_GOS.png">
                    <img v-if="isDark" class="nav_logo" alt="Vue logo" src="../assets/logo_GOS_white.png">
                </router-link>
            </div>
            <div class="link">
                <router-link class="router-link" to="/local">
                    <p v-bind:class="{ dark: isDark }">Local</p>
                </router-link>
            </div>
        </div>
        <div class="nav_bar bottom_nav">
            <router-link class="router-link" to="/archive">
                <p v-bind:class="{ dark: isDark }">Soil Archive</p>
            </router-link>
            <router-link class="router-link" to="/knowledge">
                <p v-bind:class="{ dark: isDark }">Knowledge</p>
            </router-link>
        </div>
    </div>
</template>

<script>
    export default {
      name: 'Navigation',
      data: () => {
        return {
          isDark: false
        }
      },
      watch:{
        $route (to){
          this.isDark = to.name === 'knowledge'
        }
      }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .nav {
        position: fixed;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
    }
    .nav_bar {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        padding: 25px 50px;
        width: 100%;
        position: absolute;
        left: 0;
        -webkit-box-sizing: border-box; /* Safari/Chrome, other WebKit */
        -moz-box-sizing: border-box;    /* Firefox, other Gecko */
        box-sizing: border-box;         /* Opera/IE 8+ */
    }
    .top_nav {
        top: 0;
    }
    .bottom_nav {
        bottom: 0;
    }
    .nav_logo {
        width: 250px;
        margin-top: -50px;
        cursor: pointer;
    }
    .router-link {
        text-decoration: none;
    }
    .router-link:visited {
        color: inherit;
    }
    .dark {
        color: white;
    }
</style>