<script>
export default {
    name: "AppFooter",
    props: {
        iconList: Array
    },
    data() {
        return {

        }
    }

}

</script>
<template>

    <footer>
        <div class="footer-top">
            <img src="../assets/images/avada-charity-sticky-header-logo.png" alt="">
        </div>
        <div class="footer-bottom">
            <small>&copy; copyright 2012 - 2020 AVADA THEME BY TEAM FUSION | ALL RIGHTS RESERVED | POWERED BY
                WORDPRESS</small>
            <ul class="icon-list">
                <li class="icon" v-for="(icon, index) in iconList">
                    <a href="#"><i class="fa-brands" :class="icon"></i></a>
                </li>
            </ul>


        </div>

    </footer>
</template>
<style lang= "scss" scoped>
@use "../style/partials/variables" as *;

footer {
    background-color: green;


    .footer-top {
        display: flex;
        justify-content: center;
        padding: 1rem 0;
        background-color: white;

        img {
            height: 50px;
        }
    }

    .footer-bottom {
        padding: 1rem 0;
        text-align: center;
        color: gray;
        background-color: $bg-foot-bt;

        ul {
            display: flex;
            justify-content: center;
            margin-top: 1.5rem;

            li {
                margin-right: 1.5rem;
                width: 35px;
                height: 35px;
                color: $color-bt;
                border-radius: 50%;
                background-color: white;
                line-height: 35px;
                text-align: center;
            }


        }

    }

}
</style>