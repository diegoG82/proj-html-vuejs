<script>
export default {
    name: 'AppNews'

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

            <div class="col">

                <div class="card text-center">
                    <img src="../assets/img/news/pancake-burger-400x300.jpg " alt="">
                    <h2>NEW: The Pancake Burger</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi suscipit dolore provident, iusto
                        cupiditate quo quia nesciunt repudiandae aperiam corporis distinctio libero blanditiis non ratione
                        cum? Necessitatibus deleniti alias quis?</p>
                </div>
            </div>


            <div class="col">

                <div class="card text-center">
                    <img src="../assets/img/news/new-milkshake-menu-400x300.jpg " alt="">
                    <h2>New Milkshake Menu</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi suscipit dolore provident, iusto
                        cupiditate quo quia nesciunt repudiandae aperiam corporis distinctio libero blanditiis non ratione
                        cum? Necessitatibus deleniti alias quis?</p>
                </div>
            </div>


        </div>

    </div>
</template>



<style lang="scss" scoped>
.card{
    border: none;
    p{
        font-size: 0.8rem;
    }
}
</style>