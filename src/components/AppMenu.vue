<script>
export default {
    name: 'AppMenu',

    props: {
        menucategories: Array,
    },

    methods: {
        getImage(element) {
            return new URL(`../assets/img/appmenu/${element.image}`, import.meta.url).href;
        }
    }

}
</script>


<template>
    <div class="container mt-4">
        <div class="d-flex justify-content-end"><button type="button"
                class="btn btn-danger rounded-pill text-center mb-2 mt-4">VIEW THE FULL MENU <i
                    class="fa-solid fa-circle-arrow-right"></i></button>
        </div>
        <h2 class="mt-2 ">Menu Categories</h2>
        <div class="row row-cols-4 g-2 mt-4 d-flex">
            <div class="col" v-for="(element, index) in menucategories" :key="index">
                <div class="card" :href="element.url">
                    <img :src="getImage(element)" alt="">
                    <p>{{ element.title }}</p>
                </div>
            </div>
        </div>



        <div class="cares">

            <div class="row row-cols-4 d-flex cares">



                <div class="col d-flex mt-4 justify-content-center">
                    <div class="card-cares">
                        <div class="cares-img"><img src="../assets/img/appmenu/vegan-symbol-png-5.png" alt=""></div>

                        <p class="text-center ">Vegetarian</p>
                    </div>
                </div>


                <div class="col d-flex mt-4 justify-content-center">
                    <div class="card-cares">
                        <div class="cares-img"><img src="../assets/img/appmenu/gluten-free-clip-art-8.png" alt=""></div>

                        <p class="text-center mt-2 ">Gluten Free</p>
                    </div>
                </div>

                <div class="col d-flex mt-4 justify-content-center">
                    <div class="card-cares">
                        <div class="cares-img"><img src="../assets/img/appmenu/gluten-free-clip-art-8.png" alt=""></div>

                        <p class="text-center mt-2 ">Dairy Free</p>
                    </div>
                </div>

                <div class="col d-flex mt-4 justify-content-center">
                    <div class="card-cares">
                        <div class="cares-img"><img src="../assets/img/appmenu/keto.png" alt=""></div>
                        <p class="text-center ">keto Friendly</p>
                    </div>
                </div>


            </div>




        </div>





    </div>
</template>



<style lang="scss" scoped>
.container {

    // border: 1px solid black;
    // height: 400px;

    .card {
        height: 200px;
        position: relative;

        img {
            height: 200px;
            filter: brightness(80%);

        }

        p {
            position: absolute;
            color: white;
            font-weight: 900;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

    }



}


.cares {
    height: 200px;

    .card-cares {
        width: 100px
    }
}
</style>