<template>
    <div class="nav">
        <div class="nav_bar top_nav">
            <div class="link"
                 @mouseover="hoverLink = '/global'"
                 @mouseleave="hoverLink = null">
                <router-link class="router-link" to="/global">
                    <p v-bind:class="{ dark: isDark }">Global</p>
                    <hr v-bind:class="{ dark: isDark }" v-if="!hoverLink && currentRoute === '/global' || hoverLink === '/global'">
                </router-link>
            </div>
            <div class="logo">
                <router-link v-if="currentRoute !== '/local' && currentRoute !== '/about/soil'" class="router-link" to="/about/grounds">
                    <img v-if="!isDark" class="nav_logo" alt="Vue logo" src="../assets/logo_GOS.png">
                    <img v-if="isDark" class="nav_logo" alt="Vue logo" src="../assets/logo_GOS_white.png">
                </router-link>
                <router-link v-if="!isDark && currentRoute === '/local' || currentRoute === '/about/soil'" class="router-link" to="/about/soil">
                    <img class="nav_logo" alt="Vue logo" src="../assets/logo_SIR placeholder.png">
                </router-link>
            </div>
            <div class="link"
                 @mouseover="hoverLink = '/local'"
                 @mouseleave="hoverLink = null"
            >
                <router-link class="router-link" to="/local">
                    <p v-bind:class="{ dark: isDark }">Local</p>
                    <hr v-bind:class="{ dark: isDark }" v-if="!hoverLink && currentRoute === '/local' || hoverLink === '/local'">
                </router-link>
            </div>
        </div>
        <div class="nav_bar bottom_nav">
            <div class="link"
                 @mouseover="hoverLink = '/archive'"
                 @mouseleave="hoverLink = null"
            >
                <router-link class="router-link" to="/archive">
                    <p v-bind:class="{ dark: isDark }">Soil Archive</p>
                    <hr v-bind:class="{ dark: isDark }" v-if="!hoverLink && currentRoute === '/archive' || hoverLink === '/archive'">
                </router-link>
            </div>
            <div class="link"
                 @mouseover="hoverLink = '/participate'"
                 @mouseleave="hoverLink = null"
            >
                <router-link class="router-link" to="/participate">
                    <p v-bind:class="{ dark: isDark }">participate</p>
                    <hr v-bind:class="{ dark: isDark }" v-if="!hoverLink && currentRoute === '/participate' || hoverLink === '/participate'">
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
      name: 'Navigation',
      data: () => {
        return {
          currentRoute: null,
          hoverLink: null,
          isDark: false
        }
      },
      watch:{
        $route (to){
          this.currentRoute = to.fullPath;
          this.isDark = to.name === 'participate'
        }
      },
      mounted(){
        this.currentRoute = this.$route.fullPath;
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
    hr {
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
    }
    .link {
        position: relative;
        max-height: 50px;
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
        text-transform: uppercase;
        font-weight: bold;
        color: black;
        font-size: 13px;
    }
    .router-link:visited {
        color: inherit;
    }
    .dark {
        color: white;
        border-color: white;
    }
</style>