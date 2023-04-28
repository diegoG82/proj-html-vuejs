<script>
export default {
    name: 'AppPopular',

    props: {
        maincard: Array,
    },

    methods: {
        getImage(element) {
            return new URL(`../assets/img/AppPopular/${element.image}`, import.meta.url).href;
        }
    }


}




</script>




<template>
    <section>
        <div class="container">

            <ul class="main-nav d-flex justify-content-between pt-2">
                <li><i class="fa-regular fa-clock"></i> <span>24/7 DELIVERY</span> </li>
                <li><i class="fa-solid fa-burger"></i> <span>OVER 100 DISHES</span> </li>
                <li><i class="fa-solid fa-mobile-screen-button"> </i> <span>IN APP ORDERING</span></li>
                <li><i class="fa-solid fa-car"></i> <span>FAST DELIVERY</span> </li>
            </ul>

            <div class="popular-dishes">
                <h2 class="text-center m-4">Our Most Popular Dishes</h2>
                <div class="row row-cols-3 g-4 d-flex">
                    <div class="col mycol" v-for="(element, index) in maincard" :key="index">
                        <div class="card text-center" :href="element.url">
                            <img class="card-img-top" :src="getImage(element)" alt="">
                            <div class="card-body">
                                <h5 class="card-title">{{ element.title }}</h5>
                                <p class="card-text">
                                    {{ element.price }}
                                </p>

                            </div>

                        </div>
                        <div class="addtocart">
                            <div><i class="fa-regular fa-square-check rounded-circle "></i></div>
                            <p>View Cart</p>
                        </div>

                    </div>

                </div>

            </div>

            <div class="d-flex justify-content-center"><button type="button"
                    class="btn btn-danger rounded-pill text-center">PLACE YOUR ORDER <i
                        class="fa-solid fa-circle-arrow-right"></i></button>
            </div>

        </div>

        <div class="mt-2">
            <img class="mt-2" src="../assets/img/AppPopular/firstorder.jpg" alt="">
            <img class="effect" src="../assets/img/AppPopular/svg-0.svg" alt="">
            <img class="effect-grey" src="../assets/img/AppPopular/grey.svg" alt="">
            <img class="effect-grey-center" src="../assets/img/AppPopular/grey.svg" alt="">
            <img class="effect-grey-bottom" src="../assets/img/AppPopular/grey.svg" alt="">
        </div>



    </section>

    <section></section>
</template>




<style lang="scss" scoped>
.container {
    height: 800px;
    background-color: white;
    position: relative;
    bottom: 50px;

    .main-nav {
        // border: 1px solid black;
        height: 50px;
        line-height: 50px;
        list-style: none;
        font-weight: 500;

        ul {
            list-style: none;
        }
    }

    .popular-dishes {
        height: 750px;

        .col {
            height: 100%;

            &:hover .addtocart {
                display: block;
            }
        }

        .card {
            height: 400px;

            img {
                max-width: 100%;
            }

            .card-text {
                color: red;
            }

        }



        .addtocart {
            display: none;
            height: 100px;
            width: 100px;
            text-align: center;
            position: relative;
            bottom: 150px;
            left: 160px;
            color: white;
            font-size: 1rem;




            i {
                padding: 1rem;
                font-size: 1.5rem;
                background-color: black;
            }



        }



    }




}

.mt-2 {
    position: relative;

    .effect {
        position: absolute;
        top: 5px;
        left: 0;
        z-index: 1;
    }

    .effect-grey {
        position: absolute;
        top: 40px;
        left: 0;
        opacity: 0.1;
    }

    .effect-grey-center {
        position: absolute;
        top: 60px;
        left: 0;
        opacity: 0.1;
    }

    .effect-grey-bottom {
        position: absolute;
        top: 80px;
        left: 0;
        opacity: 0.1;

    }
}
</style>