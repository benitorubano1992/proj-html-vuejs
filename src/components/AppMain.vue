<script>
import sectionValue from './sectionValue.vue';
import CardImage from './CardImage.vue';
import SectionTitle from './SectionTitle.vue';
export default {
    name: "AppMain",
    components: {
        sectionValue,
        CardImage,
        SectionTitle,
    },
    data() {
        return {
            valuesList: [{
                title: "Clean Water",
                class: "fa-droplet",
                text: "Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus"
            },
            {
                title: "Vaccinations",
                class: "fa-stethoscope",
                text: "Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus"
            },
            {
                title: "Education",
                class: "fa-graduation-cap",
                text: "Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus"


            },
            {
                title: "Farming",
                class: "fa-wheat-awn",
                text: "Nullam convalis,orci in congue aliquet diam mauris curson urna id maximum lectus magna maximus"
            }


            ],
            urlImageCause: ["avada-charity-fair-trade-featured-200x150.jpg", "avada-charity-farming-featured-200x150.jpg",
                "avada-charity-shelter-featured-200x150.jpg", "avada-charity-vaccines-featured-200x150.jpg"],
            urlImageAside: [{
                url: "photo-1444664597500-035db93e2323-177x142.jpg",
                title: " The human story of uniqueness",
                text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.Eliget,error perspiciatis libero vel odit"
            },
            {
                url: "photo-1447430617419-95715602278e-177x142.jpg",
                title: " Sustainable trade taticts",
                text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.Eliget,error perspiciatis libero vel odit"
            }
                , {
                url: "photo-1460230525622-630fe3294cd7-177x142.jpg",
                title: "Farmers Making difference",
                text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.Eliget,error perspiciatis libero vel odit"
            }
                , {
                url: "photo-1460600421604-5e138c208b9c-177x142.jpg",
                title: "Meeting remote tributes in Peru",
                text: "Lorem ipsum dolor sit amet consectetur adipisicing elit.Eliget,error perspiciatis libero vel odit"
            }

            ],
            TitleSection: [
                {
                    titolo: "Recent Causes",
                    sottotit: "30 contries in 5 continets"
                },
                {
                    titolo: "Latest Article",
                    sottotit: "Together we all make difference"
                },
                {
                    titolo: "Change you Life Today",
                    sottotit: "As long as Poverty,Injustice&inequality persist,none of us can truly rest.it doesn't take much to changea life.Get in touch today and start making the difference"
                }



            ]

        }

    }
}
</script>
<template>
    <section class="content">


        <div class="descr-content">
            <div class="container">
                <h2>Every Moment count</h2>
                <p class="content-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto quidem impedit
                    maiores,
                    recusandae
                    molestiae deleniti provident itaque quas rem vitae cupiditate.
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
                    !</p>
                <p class="content-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora quod atque
                    beatae
                    pariatur quae
                    provident quo numquam vero distinctio accusamus, placeat cupiditate soluta nam expedita nisi. Ut aut
                    commodi explicabo.

                </p>
                <p class="content-text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsam at provident
                    vero
                    natus quasi! Maxime
                    laudantium distinctio</p>
                <a href="#" class="btn btn-action"> Our Mission</a>
            </div>
        </div>

        <div class="result-number">
            <ul>
                <li><span><i class="fa-regular fa-heart"></i> 2032</span><span>Volunteers WorldWide</span></li>
                <li><span><i class="fa-solid fa-dollar-sign"></i>132</span><span>Active Projects</span></li>
                <li><span><i class="fa-solid fa-dollar-sign"></i>3.8 M</span><span>Donated</span></li>
            </ul>
        </div>




    </section>

    <sectionValue :listValues="valuesList" />
    <section class="last-causes">
        <div class="container">

            <SectionTitle :testo="TitleSection[0]" class="text-center" />
            <div class="slider-image">
                <div class="image-box" v-for="(url, index) in urlImageCause" :key="index">
                    <CardImage :imageUrl="url" />
                </div>
            </div>

        </div>
    </section>

    <section class="aside-causes">
        <p>view all our causes</p>
    </section>

    <section class="latest-article">
        <div class="container-small">
            <SectionTitle :testo="TitleSection[1]" />
            <div class="row">
                <div class="col-big">
                    <div class="card card-big">
                        <div class="card-image">
                            <img src="../assets/images/photo-1444213007800-cff19e1677ac-600x450.jpg" alt="">
                        </div>
                        <div class="card-box-text">
                            <p class="title-card-box-text">
                                Understand comunities complexities
                            </p>
                            <p class="sub-title">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi,
                                error perspiciatis
                                libero vel odit </p>
                        </div>

                    </div>
                </div>
                <div class="col-aside-card">
                    <div class="card card-sm" v-for="(card, index) in urlImageAside" :key="index">
                        <div class="card-image-box">
                            <CardImage :imageUrl="card.url" />
                        </div>
                        <div class="card-text">
                            <p class="title-card-box-text">
                                {{ card.title }}
                            </p>
                            <p class="sub-title">{{ card.text }}</p>
                        </div>
                    </div>


                </div>

            </div>
            <a href="#" class="aside-causes">view all our articles</a>

        </div>

    </section>

    <section class="aside">
        <div class="container-sm-aside">
            <SectionTitle :testo="TitleSection[2]" />
            <div class="action-btn">
                <ul>
                    <li><a href="#" class="btn btn-interaction">Our Mission</a></li>
                    <li><a href="#" class="btn btn-interaction">Donate NOW</a></li>
                </ul>
            </div>

        </div>

    </section>






</template>
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.content {
    display: flex;
}

.descr-content {
    width: 75%;
    padding: 2.5rem 0;
    background-color: white;

    h2 {
        text-transform: uppercase;
        font-weight: 100;
        position: relative;
        padding-bottom: 20px;

        &:after {
            content: "";
            display: inline-block;
            width: 125px;
            background-color: $color-bt;
            height: 3px;
            position: absolute;
            bottom: 0;
            left: 0;
        }


    }

}


.result-number {
    width: 25%;
    padding: 2.5rem 0;
    background-image: url(../assets/images/home-content-bg-1.jpg);
    background-size: cover;

    li {
        display: flex;
        flex-direction: column;
        color: white;
        align-items: center;
        margin-bottom: 3rem;




        &>span:first-child {
            font-size: 1.5rem;
        }



    }

    li:nth-of-type(3) {
        margin-bottom: 0;
    }


}

.content-text {
    font-size: 0.8rem;
    line-height: 1.6;
    margin-top: 1.2rem;

    &:nth-of-type(3) {
        margin-bottom: 1.2rem;
    }

}






.last-causes {
    padding: 2.5rem 0;
    text-align: center;
    background-color: white;



    .slider-image {
        display: flex;
        justify-content: space-between;

        .image-box {
            width: calc(100% / 4 - 20px);
            height: 200px;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

    }
}

.aside-causes {
    height: 50px;

    background-color: $bg-red;
    color: white;
    text-transform: uppercase;
    line-height: 50px;
    text-align: center;

}



/*sezione card */

.latest-article {
    background-color: white;
    padding: 2rem 0;





    .col-big {
        border: none;

        .card-big {
            .card-image {
                height: 80%;

                img {
                    height: 100%;
                    width: 100%;
                    object-fit: cover;
                }

            }

            .card-box-text {
                padding: 1rem 0.5rem;
                font-size: 0.8rem;

                .sub-title {
                    margin-top: 0.6rem;
                }



            }

        }

    }





}


.col-aside-card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    border: none;
}

.card-sm {



    &:last-child {
        margin-bottom: 0;
    }

    .card-image-box {
        width: 35%;
    }

    img {
        display: block;
        height: 100%;
        object-fit: cover;
    }

    .card-text {
        font-size: 0.8rem;
        padding: 0.6rem 0 0.6rem 0.6rem;

        .sub-title {
            line-height: 1.5;
            margin-top: 0.8rem;
        }
    }

}



a.aside-causes {
    display: block;
    margin-top: 1.2rem;
    height: 30px;
    line-height: 30px;
}




/*aside-section */
.aside {

    color: white;
    background-image: url(../assets/images/home-footer.jpg);
    background-position: center;
    height: 500px;
    display: flex;
    align-items: center;

    .container-sm-aside {
        width: 50%;
        margin: 0 auto;
        text-align: center;


    }


    ul {
        display: flex;
        justify-content: center;
        margin-top: 1.5rem;

        li:first-child {
            margin-right: 1rem;
        }

    }

}
</style>