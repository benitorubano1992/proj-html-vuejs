<script>
export default {
    name: "sectionValue",
    props: {
        listValues: Array,
    },
    Data() {
        return {

        }
    }

}</script>
<template>
    <section class="value-company">
        <div class="container">
            <h2>Our Values</h2>
            <p>Thimk Big Act Bigger</p>
            <ul class="list-values">
                <li v-for="(value, index) in listValues" :key="index">
                    <i class="fa-solid" :class="value.class"></i>
                    <span>{{ value.title }}</span>
                    <p>{{ value.text }}</p>
                    <a href="#" class="btn btn-action">Learn More</a>
                </li>
                <!--<li>
                    <i class="fa-solid fa-stethoscope"></i>
                    <span>Vaccinations</span>
                    <p>Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus
                    </p>
                    <a href="#" class="btn btn-action">Learn More</a>
                </li>
                <li>
                    <i class="fa-solid fa-graduation-cap"></i>
                    <span>Education</span>
                    <p>Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus
                    </p>
                    <a href="#" class="btn btn-action">Learn More</a>
                </li>
                <li>
                    <i class="fa-solid fa-graduation-cap"></i>
                    <span>Education</span>
                    <p>Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus
                    </p>
                    <a href="#" class="btn btn-action">Learn More</a>
                </li>
            -->

            </ul>


        </div>



    </section>


</template>
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.value-company {
    padding: 3rem 0;
    text-align: center;
    color: white;
    background-image: url(../assets/images/home-content-bg-2.jpg);
    background-size: cover;
    height: 400px;
    background-position: center;

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
    }

    p {
        margin-top: 1rem;
    }

    .list-values {
        margin-top: 3rem;
        display: flex;
        justify-content: space-between;

        li {
            width: 22.5%;
            display: flex;
            flex-direction: column;
            align-items: center;

            i {
                font-size: 1.8rem;
                margin-bottom: 0.6rem;
                color: $color-bt;
            }


            p {
                margin: 1.4rem 0;
                font-size: 0.7rem;
                line-height: 1.5;

            }

            a {
                display: inline;
            }
        }

    }
}
</style>
