<template>
    <section class="my-5 py-5">
        <div class="container">
            <div class="row align-items-center gy-5">
                <div class="left-top col-12 col-lg-7 col-xl-6">
                    <h6 class="mb-4 fw-bold ">Category</h6>
                    <h3 class="text-primary w-100 mb-4 fw-bold ">Lorem ipsum dolor sit amet consectetur adipisicing
                        elit.
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero, dolore.
                    </h3>
                    <p class="w-100 my-txt-semi-dark">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae
                        nihil libero,
                        asperiores tempore
                        magnam nostrum labore fugit at delectus vel autem explicabo impedit cum, recusandae id ad. Enim
                        ipsum amet quis quae commodi eum natus, architecto fugiat delectus? Ipsa, laboriosam.</p>

                    <button class="btn primary-button rounded-5 my-4">Read More</button>
                </div>
                <div class="right-bottom col-12 col-lg-5 col-xl-6">
                    <img class="img-fluid" src="./../../images/gallery-1.jpg" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "TopSections",
}
</script>

<style lang="scss" scoped>
img {
    aspect-ratio: 1 / 1;
    object-fit: cover;
}

@media (min-width: 778px) {

    .left-top h3,
    p {
        width: 90% !important;
    }
}
</style>