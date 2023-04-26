<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/Appmain.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppNews from './components/Appnews.vue';
import AppFooter from './AppFooter.vue';
import { store } from './store.js'
export default {
  data() {
    return {

      headermenu: [
        { menutext: 'Home' },
        { menutext: 'Order Online' },
        { menutext: 'About' },
        { menutext: 'News' },
        { menutext: 'Contact us' },
       ],

    }

  },
  components: {
    AppHeader,
    AppMain,
    AppJumbo,
    AppNews,
    AppFooter,
  },

}
</script>


<template>
  <!-- AppHeader -->
  <AppHeader :headermenu = "headermenu"  />
  <!-- AppMain -->
  <AppMain />
  <!-- AppJumbo -->
  <AppJumbo />
  <!-- AppNews -->
  <AppNews />
  <!-- AppFooter -->
  <AppFooter />
</template>

<style lang="scss">
@use "./style.scss" as *;
</style>