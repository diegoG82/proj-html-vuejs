<script>
export default {
    name: 'AppFooter',

    props: {
        orderonline: Array,
        menunavigate: Array,
        menuinfo: Array,
        menuhours: Array,
    },


}
</script>




<template>
    <div class="footer mt-4">

        <div class="ms_container d-flex">

            <ul class=" justify-content-between mt-4">
                <li class="mb-4 text-uppercase">ORDER ONLINE</li>
                <li class="mb-2" v-for="(element, index ) in orderonline" :key="index">{{ element.text }}</li>
            </ul>

            <ul class=" justify-content-between mt-4">
                <li class="mb-4 text-uppercase">NAVIGATE</li>
                <li class="mb-2" v-for="(element, index) in menunavigate" :key="index">{{ element.text }}</li>

            </ul>

            <ul class=" justify-content-between mt-4">
                <li class="mb-4 text-uppercase">INFORMATION</li>
                <li class="mb-2" v-for="(element, index) in menuinfo" :key="index">{{ element.text }}</li>
                <li class="mb-2"><img class="logo" src="./assets/img/AppFooter/app-store-badge.png" alt=""></li>
                <li class="mb-2"><img class="logo" src="./assets/img/AppFooter/play-store-badge.png" alt=""></li>

            </ul>

            <ul class=" justify-content-between mt-4">
                <li class="mb-4 text-uppercase">OPENING HOURS</li>
                <li class="mb-2" v-for="(element, index) in menuhours" :key="index">{{ element.day }} <span
                        class="yellow">{{ element.text }}</span> </li>
            </ul>





            <ul class=" justify-content-between mt-4 text-center">
                <li>VOUCHER</li>
                <li><img src="./assets/img/AppFooter/footer-coupon-200x200.png" alt=""></li>
                <li>JustUseTheCode</li>
                <li class="yellow">FIRSTORDER</li>
                <li>AtCheckout</li>
            </ul>




        </div>


        <div class="bottom-footer text-center">
            <img class="mb-2" src="../src/assets/img/AppFooter/takeout-logo.png" alt="">
            <h2 class="yellow">Stay In The Loop</h2>
            <p class="text-white">Sign up to receive up to date news and offers directly in your inbox
            </p>
            <input class="input" type="text" placeholder="you@email.com">
            <div><button type="button" class="btn btn-danger rounded-pill text-center mb-2 mt-2">SUBSCRIBE</button></div>
            <div class="social text-white">
                <ul class="d-flex justify-content-center g-4">
                    <li><i class="fa-brands fa-facebook"></i></li>
                    <li><i class="fa-brands fa-twitter"></i></li>
                    <li><i class="fa-brands fa-instagram"></i></li>
                    <li><i class="fa-brands fa-linkedin"></i></li>
                    <li><i class="fa-solid fa-rss"></i></li>
                    <li><i class="fa-brands fa-youtube"></i></li>
                    <li><i class="fa-regular fa-envelope"></i></li>
                </ul>
            </div>

            <p class="credits"><i class="fa-regular fa-copyright"></i> Copyright 2012-2020 avada theme by <span class="text-white">ThemeFusion</span> All rights reserved Powered by <span class="text-white">WordPress</span></p>



        </div>


    </div>
</template>



<style lang="scss" scoped>
.footer {
    height: 1000px;
    background-image: url(./assets/img/AppFooter/footer-background-scaled.jpg);
    background-size: cover;
    background-position: center bottom;

    .ms_container {
        height: 400px;
        // border: 1px solid white;
        width: 80%;
        margin: 0 auto;

        ul {
            color: white;
            list-style: none;
            // border: 1px solid white;
            height: 350px;
            width: calc(100% / 5);
            padding: 1rem;

            .yellow {
                color: yellow;
            }

            // text-align: center;
            .logo {
                border: 1px solid white;
                border-radius: 5px;
                width: 40%;
            }


        }

    }

    .bottom-footer {
            margin: 0 auto;
        height: 300px;
        width: 600px;

        img {
            width: 30%
        }

        .yellow {
            color: yellow;
        }

        .input {
            width: 80%;
            border-radius: 10px;
        }

        button {
            width: 80%;
            padding: 0.2rem
        }

        ul {
            list-style: none;
            color: white;
            padding-left: unset;
            gap:10px;   
            font-size:1.5rem ;
            margin:2    rem;
        }
        .credits{
            color:yellow;
            font-size: 0.8rem;
     
        }


    }
}</style>