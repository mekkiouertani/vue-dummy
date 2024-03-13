<template>
    <section class="my-bg-light py-5">
        <div class="container y-5">
            <h3 class="text-primary fw-bold">Latest from the blog</h3>
            <p class="w-100 my-txt-semi-dark my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Esse cumque
                pariatur dignissimos
                soluta
                necessitatibus numquam saepe molestias est, itaque ipsum natus. Earum recusandae mollitia nostrum beatae
                velit!</p>
            <div class="row my-4 g-5 justify-content-center">
                <div class="col-12  col-lg-6 col-xl-4" v-for="card in cards">
                    <div class="my-card ">
                        <div class="box-img">
                            <img :src="card.image" class="img-fluid" :alt="card.title" />
                        </div>
                        <div class="info fw-bold px-4 p-3 mt-3">
                            <h2 class="fs-5 text-primary fw-bold ">{{ card.category }} <span
                                    class="my-txt-semi-dark  fs-6"> / {{ card.date }}</span></h2>
                            <p class="text-secondary fw-light pt-2 text-dark fw-bolder fs-6">Lorem ipsum dolor sit, amet
                                consectetur adipisicing
                                elit. Fuga in a quia
                                voluptatem quidem est?</p>
                            <small><span class="bg-primary"></span>Read
                                more <span class="bg-primary"></span></small>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "MiddleSection",
    data() {
        return {
            cards:
                [
                    {
                        image: '/public/images/carousel/s1.jpg',
                        category: 'Nature',
                        title: 'NatureLorem ipsum dolor sit amet consectetur adipisicing elit.',
                        date: 'March 13, 24',
                    },
                    {
                        image: '/public/images/carousel/s2.jpg',
                        category: 'Woods',
                        title: 'Woods ipsum dolor sit amet consectetur adipisicing elit.',
                        date: 'March 14, 24',
                    },
                    {
                        image: '/public/images/carousel/s3.jpg',
                        category: 'Sun',
                        title: 'Sun  ipsum dolor sit amet consectetur adipisicing elit.',
                        date: 'March 15, 24',
                    },
                ]
        }
    },
}
</script>

<style lang="scss" scoped>
.my-card {

    color: black;
    background-color: white;
    display: flex;
    flex-direction: column;
    padding: 0px;
    /* aspect-ratio: 3 / 3.3; */
    overflow: hidden;


    .box-img {
        aspect-ratio: 16 / 9;
        width: 100%;
        min-height: 20%;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
}

// Read more effect HOVER
small span {
    display: inline-block;
    width: 15%;
    height: 2px;
    margin-left: 5%;
    transition: 0.2s linear;
}

small {
    cursor: pointer;

    span:first-child {
        width: 0% !important;
        margin: 0% !important;

    }

    small:hover span {
        width: 15% !important;
    }
}

small:hover>span:last-child {
    width: 0%;
}

small:hover>span:first-child {
    width: 15% !important;
    margin-right: 5% !important;
}


@media (min-width: 778px) {
    .my-txt-semi-dark {
        width: 70% !important;
    }
}
</style>