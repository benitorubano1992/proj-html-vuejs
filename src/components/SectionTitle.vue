<script>
export default {
    name: "SectionTitle",
    props: {
        testo: Object
    },
    data() {
        return {

        }
    }
}
</script>
<template>
    <h2>{{ testo.titolo }}</h2>
    <p>{{ testo.sottotit }}</p>

</template>
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

h2 {
    text-transform: uppercase;
    padding-bottom: 1.3rem;
    position: relative;

    &::after {
        content: "";
        display: inline-block;
        width: 140px;
        height: 3px;
        background-color: $color-bt;
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
    }
}

h2,
p {
    font-weight: 200;
    text-align: center;
}

p {
    margin-top: 1rem;
    margin-bottom: 2.5rem;
}
</style>