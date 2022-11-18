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
            <div class="icon-list">
                <div class="icon" v-for="(icon, index) in iconList">
                    <i class="fa-brands" :class="icon"></i>
                </div>
            </div>


        </div>

    </footer>
</template>
<style lang= "scss" scoped>
@use "../style/partials/variables" as *;

footer {
    background-color: green;
}

.footer-top {
    display: flex;
    justify-content: center;
    padding: 1rem 0;
    background-color: white;

    img {
        height: 50px;
    }
}
</style>