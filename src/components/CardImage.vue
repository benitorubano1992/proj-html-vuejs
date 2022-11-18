<script>
export default {
    name: "CardImage",
    props: {
        imageUrl: String,
    },
    data() {
        return {

        }
    }, methods: {
        getImagePath: function (url) {
            return new URL(url, import.meta.url).href;
        }
    }


}
</script>
<template>
    <div class="card-image">
        <img :src="getImagePath(`../assets/images/${imageUrl}`)" alt="">
    </div>

</template>
<style lang="scss" scoped>
.card-image {
    width: 100%;
    height: 100%;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
</style>
