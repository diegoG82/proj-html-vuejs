<script>
import AppHeader from './components/AppHeader.vue';
import AppPopular from './components/AppPopular.vue';
import AppMenu from './components/AppMenu.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppNews from './components/Appnews.vue';
import AppFooter from './AppFooter.vue';
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

      ],

      menucategories: [
        {
          image: 'appetizers-menu-background.jpg',
          title: 'APPETIZERS'
        },

        {
          image: 'burgers-menu-background.jpg',
          title: 'BURGERS'
        },

        {
          image: 'pizza-menu-background.jpg',
          title: 'PIZZA'
        },

        {
          image: 'fries-menu-background.jpg',
          title: 'FRIES'
        },

        {
          image: 'sides-menu-background.jpg',
          title: 'SIDES'
        },

        {
          image: 'desserts-menu-background.jpg',
          title: 'DESSERTS'
        },

        {
          image: 'beverages-menu-background.jpg',
          title: 'BEVERAGES'
        },

        {
          image: 'specials-menu-background.jpg',
          title: 'SPECIALS'
        },

      ],

      orderonline: [
        {
          text: 'Appetizer'
        },

        {
          text: 'Burgers'
        },

        {
          text: 'Pizzas'
        },

        {
          text: 'Fries'
        },

        {
          text: 'Sides'
        },

        {
          text: 'Desserts'
        },

        {
          text: 'Beverage'
        },

        {
          text: 'Specials'
        },


      ],


      newsmenu:[
        {
          image: 'pancake-burger-400x300.jpg',
          title: 'NEW: The Pankake Burger',
          text:'Our new Pancake Burger, made by two burgers inside our fresh pancakes, premium cheddar, garlic and our home made sauce. '
        },

        {
          image: 'new-milkshake-menu-400x300.jpg',
          title:'New Milkshake Menu',
          text:'Enjoy our new Milkshake menu with an huge choice of tastes, topping and three different size at your service.'
        },

      ],

      menunavigate: [
        {
          text: 'Home'
        },

        {
          text: 'Alternate Home'
        },

        {
          text: 'Menu'
        },

        {
          text: 'About'
        },

        {
          text: 'News'
        },

        {
          text: 'Contact Us'
        },

        {
          text: 'Cart'
        },
      ],

      menuinfo: [
        {
          text: 'My Account'
        },

        {
          text: 'Privacy Policy'
        },

        {
          text: 'Terms of Service'
        },


      ],



      menuhours: [
        {
          day: 'Mon - ',
          text: ' 10AM to 11PM'
        },

        {
          day: 'Tue -',
          text: '  10AM to 11PM'
        },

        {
          day: 'Wed -',
          text: '    10AM to 11PM'
        },

        {
          day: 'Thur -',
          text: ' 10AM to 11PM'
        },

        {
          day: 'Fri -',
          text: ' 10AM to 11PM'
        },

        {
          day: 'Sat -',
          text: ' 10AM to 11PM'
        },

        {
          day: 'Sun -',
          text: ' 11AM to 11PM'
        },



      ],

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
  <AppMenu :menucategories="menucategories" />
  <!-- AppJumbo -->
  <AppJumbo />
  <!-- AppNews -->
  <AppNews :newsmenu="newsmenu" />
  <!-- AppFooter -->
  <AppFooter :orderonline="orderonline" :menunavigate="menunavigate" :menuinfo="menuinfo" :menuhours="menuhours" />
</template>

<style lang="scss">
@use "./style.scss" as *;

body {
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
}
</style>