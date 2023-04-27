<script>
import AppHeader from './components/AppHeader.vue';
import AppPopular from './components/AppPopular.vue';
import AppMenu from './components/AppMenu.vue';
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

      maincard: [
        {
          image: 'skin-on-fries-400x571.jpg',
          title: 'Skin on fries',
          price: '$3.00-$6.00',
        },

        {
          image: 'choco-cookie-frappe-400x571.jpg',
          title: 'Choco Cookie Frappe',
          price: '$4.99',
        },

        {
          image: 'donut-burger-400x571.jpg',
          title: 'The Donut Burger',
          price: '$6.99',
        },

      ]

    }

  },
  components: {
    AppHeader,
    AppPopular,
    AppMenu,
    AppJumbo,
    AppNews,
    AppFooter,
  },

}
</script>


<template>
  <!-- AppHeader -->
  <AppHeader :headermenu="headermenu" />
  <!-- AppPopular -->
  <AppPopular :maincard="maincard" />
  <!-- AppMenu -->
  <AppMenu/>
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