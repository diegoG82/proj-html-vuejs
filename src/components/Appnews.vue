<script>
export default {
    name: 'AppNews',

    props: {
        newsmenu: Array,
    },

    methods: {
        getImage(element) {
            return new URL(`../assets/img/news/${element.image}`, import.meta.url).href;
        }
    }

}
</script>




<template>
    <div class="container mt-4">
        <div class="d-flex justify-content-end"><button type="button"
                class="btn btn-danger rounded-pill text-center mb-2 mt-4">READ MORE NEWS <i
                    class="fa-solid fa-circle-arrow-right"></i></button>
        </div>
        <h2>Latest News</h2>

        <div class="row row-cols-2 g-4 mt-4 d-flex">

            

            <div class="col" v-for="(element, index) in newsmenu" :key="index">

                <div class="card text-center" :href="element.url">
                    <img :src="getImage(element)" alt="">
                    <h2 class="mt-4">{{ element.title }}</h2>
                    <p>{{ element.text }}</p>
                </div>
            </div>





        </div>

    </div>
</template>



<style lang="scss" scoped>
.card {
    border: none;

    // p {
    //     font-size: 0.8rem;
    // }
}
</style>