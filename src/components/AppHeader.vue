<script>
export default {
    name: "AppHeader",
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
                        <li><a href="#" class="active">home</a></li>
                        <li><a href="#">mission</a></li>
                        <li><a href="#">causes</a></li>
                        <li><a href="#">journal</a></li>
                        <li><a href="#" class="btn btn-action">donate</a></li>
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
header {
    background-color: black;
    color: white;
    font-weight: lighter;
    background-image: url(../assets/images/home-page-slider.jpg);
    background-size: cover;
    height: 100vh;

    .container {
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
        min-height: 200px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        h1,
        p {
            margin-top: 1rem;
        }

        .action-btn {
            margin-top: 1.5rem;

            ul {
                display: flex;
                justify-content: center;

                li:first-child {
                    margin-right: 1rem;

                }

            }



        }

    }
}
</style>