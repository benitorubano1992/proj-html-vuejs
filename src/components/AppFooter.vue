<script>
export default {
    name: "AppFooter",
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
    </footer>
</template>
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

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