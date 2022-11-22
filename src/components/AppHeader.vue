<script>
export default {
    name: "AppHeader",
    props: {
        listLinks: Array
    },
    data() {
        return {

        }

    },
    methods: {
        getImagePath: function (url) {
            return new URL(url, import.meta.url).href;
        }
    }
}
</script>
<template>
    <header>


        <div class="container">
            <div class="header-top">
                <div class="header-logo">
                    <img :src="getImagePath('../assets/images/avada-charity-logo.png')" alt="logo-avada-charity">
                </div>
                <nav>
                    <ul>
                        <li v-for="(link, index) in listLinks" :key="index">
                            <a :href="link.href" :class="{ 'active': link.active, 'btn btn-action': index === 4 }">{{
                                    link.title
                            }}</a>
                        </li>

                        <!--
                        <li><a href="#" class="active">home</a></li>
                        <li><a href="#">mission</a></li>
                        <li><a href="#">causes</a></li>
                        <li><a href="#">journal</a></li>
                        <li><a href="#" class="btn btn-action">donate</a></li>
                        -->
                    </ul>
                </nav>
            </div>
            <div class="jumbotron">

                <div class="text-center">
                    <h1>Make a Difference</h1>
                    <p>As long as Poverty,Injustice&inequality persist,none of us can truly rest</p>

                    <div class="action-btn">
                        <ul>
                            <li><a href="#" class="btn btn-interaction">Our Mission</a></li>
                            <li><a href="#" class="btn btn-interaction">Donate NOW</a></li>
                        </ul>
                    </div>
                </div>

            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

header {
    background-color: black;
    color: white;
    font-weight: lighter;
    position: relative;
    background-image: url(../assets/images/home-page-slider.jpg);
    background-size: cover;

    background-repeat: no-repeat;
    height: 500px;



    img .container {
        width: 90%;
        margin: 0 auto;
    }

    .header-top {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.6rem 0;


        .header-logo {
            img {
                height: 50px;
            }
        }

        ul {
            display: flex;
            text-transform: uppercase;

            li:not(:last-child) {
                margin-right: 2.5rem;

            }


        }


    }

    .jumbotron {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        z-index: 999;

        h1,
        p {
            margin-top: 1rem;
        }

        p {
            margin-bottom: 2rem;
        }

        .action-btn {
            margin-top: 2rem;

            ul {
                display: flex;
                justify-content: center;

                li:first-child {
                    margin-right: 1rem;

                    .btn {
                        color: $color-bt;
                        border-color: $color-bt;
                    }
                }

            }



        }

    }
}
</style>