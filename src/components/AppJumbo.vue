<script>
export default {

}
</script>




<template>
    <div class="jumbotron d-flex">
        <div class="jumbo-container d-flex justify-content-center align-self-center">
            <div>
                <h3>Download our</h3>
                <h2>Ordering App</h2>
                <img class="mt-4 " src="../assets/img/jumbo/app-store-badge-200x67.png" alt="">
                <img class="pl-4 mt-4"  src="../assets/img/jumbo/play-store-badge-200x67.png" alt="">
            </div>

        </div>

    </div>
</template>



<style lang="scss" scoped>
.jumbotron {
    height: 500px;
    background-image: url(../assets/img/jumbo/app-ordering-scaled.jpg);
    background-size: cover;
    background-position: center bottom;

    .jumbo-container {
            // border: 1px solid black;
        height: 300px;
        width: 55%;

        h3{
            font-size:1.2rem;
            color:white;
        }

        h2{
            font-size: 3rem;
            color: yellow;
        }

        img{
            width:25%;
            margin-right: 1rem;
        }

    }
}
</style>