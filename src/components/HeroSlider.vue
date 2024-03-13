<template>
    <div id="carouselExampleCaptions" class="carousel slide ">
        <div class="carousel-inner">
            <!-- SLIDE -->
            <div class="carousel-item active" v-for="(slide, index) in  slides " :key="index">
                <img :src="slide.image" :alt="slide.title" role="img" preserveAspectRatio="xMidYMid slice"
                    focusable="false">
                <title>{{ slide.title }}</title>
                <div class="carousel-caption  text-start ">
                    <h6 class="my-4 ">{{ slide.category }}</h6>
                    <h2 class="fw-bold mb-5 fs-1">{{ slide.title }}</h2>
                    <p class="d-none d-md-block">{{ slide.description }}</p>
                    <button class="my-4 d-none d-md-block btn primary-button rounded-5 ">Read More</button>
                </div>
            </div>
        </div>
        <!-- navigation arrows -->
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" style="" aria-hidden="true"></span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
        </button>
    </div>
</template>

<script>
export default {
    name: 'HeroSlider',
    data() {
        return {
            slides: [
                {
                    image: '/public/images/carousel/s1.jpg',
                    category: 'Nature',
                    title: 'Nature Lorem ipsul dolor sit amet, consetetur',
                    description: ' Nature Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla ut provident laudantium. Pariatur accusamus omnis quam id iste quasi incidunt'
                },
                {
                    image: '/public/images/carousel/s2.jpg',
                    category: 'Woods',
                    title: 'Woods Lorem ipsul dolor sit amet, consetetur',
                    description: 'Woods Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla ut provident laudantium. Pariatur accusamus omnis quam id iste quasi incidunt'
                },
                {
                    image: '/public/images/carousel/s3.jpg',
                    category: 'Sun',
                    title: 'Sun Lorem ipsul dolor sit amet, consetetur',
                    description: ' Sun Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla ut provident laudantium. Pariatur accusamus omnis quam id iste quasi incidunt'
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.carousel {
    overflow: hidden;
}

.carousel-item {
    max-height: 800px;
    width: 100%;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}

.carousel-caption {
    top: 20%;
    transform: translate(0, -20%);
    width: 60% !important;
}

//navigation arrows 
.carousel-control-prev-icon,
.carousel-control-next-icon {
    transform: scaleY(2);

}

.carousel-control-prev {
    left: -4%;
    position: absolute;
}

.carousel-control-next {
    right: -4%;
}

.primary-button {
    &:hover {
        background-color: #fff !important;
        color: black !important;
    }
}

@media (min-width: 768px) {

    //navigation arrows 
    .carousel-control-prev {
        left: -6%;
        margin: 0 !important;
    }

    .carousel-control-next {
        right: -6%;
        margin: 0 !important;
    }

    .carousel-caption {
        top: 10%;
        transform: translate(0, -10%);
        width: 60% !important;
    }

}

@media (min-width: 992px) {
    .carousel-caption {
        top: 40%;
        transform: translate(0, -40%);
        width: 50% !important;
    }
}

@media (min-width: 1200px) {
    .carousel-caption {
        top: 50%;
        transform: translate(0, -50%);
        width: 40% !important;
    }
}
</style>