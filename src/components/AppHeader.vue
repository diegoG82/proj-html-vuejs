<script>
export default {
    name: 'AppHeader',

    props: {
        headermenu: Array,
    },

}
</script>


<template>
    <div class="header">
        <div class="add d-flex"><i class="fa-solid fa-circle-plus fa-2x"></i></div>
        <div class="container header-list d-flex">
            <div class="logo">
                <img src="../assets/img/Header/takeutlogo.png" alt="">
            </div>
            <div class="header-menu">
                <ul class="d-flex justify-content-between">

                    <li v-for="(element, index) in headermenu" :key="index">
                        <span id="list"> {{ element.menutext }}</span> <i class="fa-solid fa-chevron-down"></i>
                    </li>
                    <li><i class="fa-solid fa-cart-shopping"></i></li>


                </ul>
            </div>

        </div>

        <div class="header-icons mt-4 d-flex flex-column align-items-end">

            <img class="mb-2" src="../assets/img/Header/img1.png" alt="">
            <img src="../assets/img/Header/img2.png" alt="">

        </div>



        <div class="container main-header mt-4 ">
            <h3>Hungry?</h3>
            <h2 class="header-title">Great Food</h2>
            <h2>Delivered</h2>
            <button type="button" class="btn btn-danger rounded-pill">VIEW OUR MENU <i
                    class="fa-solid fa-circle-arrow-right"></i></button>

        </div>


    </div>
</template>



<style lang="scss" scoped >
.header {
    background: url(../assets/img/Header/headerimg.jpg);
    background-size: cover;
    background-position: center bottom;
    height: 900px;

    .add {
        height: 50px;
        justify-content: end;

        i {
            color: red;
            margin: 5px;
        }
    }

    .header-icons {
        img {
            width: 2%;
            margin-right: 5px;
            border-radius: 5px;
        }

    }

    .header-list {
        width: 100%;
        height: 50px;

        .logo {
            line-height: 50px;
            width: 30%;

        }

        .header-menu {
            width: 70%;
            line-height: 50px;
            color: white;

            ul {
                list-style: none;

                .fa-chevron-down {
                        // display: none;
                    opacity:0 ;

                }

                li:hover i {
                    color: yellow;
                    display: inline-block;
                    opacity: 1;
                }

                li:hover #list {
                    color: yellow;

                }

            }
        }


    }

    .header-icons {

        height: 100px;
        color: white;

    }

    .main-header {

        height: 300px;
        color: white;

        h2 {
            font-size: 3rem;
        }

        .header-title {
            color: yellow;
            font-size: 3.5rem;
        }

        button {
            font-size: 0.7rem;
        }
    }
}
</style>