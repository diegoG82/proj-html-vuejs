<script>
    export default {
        name:'AppFooter',

        props: {
        orderonline: Array,
    },

        
    }
</script>




<template>

<div class="footer mt-4">

    <div class="ms_container d-flex">
      
        <ul class=" justify-content-between mt-4">
            <li class="mb-2">ORDER ONLINE</li>
            <li v-for="(element, index ) in orderonline" :key="index">{{ element.text }}</li>
        </ul>

        <ul class=" justify-content-between mt-4">
            <li>ciao</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>

        <ul class=" justify-content-between mt-4">
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>

        <ul class=" justify-content-between mt-4">
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>

        <ul class=" justify-content-between mt-4">
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>

       
    </div>


</div>
    
</template>



<style lang="scss" scoped>

.footer{
    height:800px;
    background-image: url(./assets/img/AppFooter/footer-background-scaled.jpg);
    background-size: cover;
    background-position: center bottom;

    .ms_container{
        height:800px;
        border:1px solid white;
        width:80%;
        margin:0 auto;
        ul{
            color:white;
            list-style: none;
            border:1px solid white;
            height:500px;
            width: calc(100% / 5);
            padding:2rem;
            // text-align: center;
        }
        
    }
}



</style>