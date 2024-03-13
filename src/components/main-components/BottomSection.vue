<template>
    <section class="container-fluid bg-primary">
        <div class="row gx-0 align-items-stretch">
            <div class="right-top col-12  col-lg-6   ">
                <img class="align-self-stretch" src="./../../images/winter.jpg" alt="winter-pic">
            </div>
            <div class="left-bottom  col-12  col-lg-6 text-white p-5 position-relative">
                <div class="position-absolute">
                    <h6 class="pt-4">On focus</h6>
                    <h3 class="w-75 my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore, sed.</h3>
                    <p class="w-75">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Totam labore ea aliquid
                        atque,
                        distinctio
                        ex veniam blanditiis dolor quis, velit vel ipsam. Impedit asperiores facilis aliquam accusamus
                        ea,
                        laudantium sunt architecto quae alias amet id libero accusantium possimus! Nesciunt, suscipit!
                    </p>
                    <button class="btn primary-button rounded-5">Read More</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'BottomSections',
}
</script>

<style lang="scss" scoped>
@use './../../../src/assets/style/partials/variables' as *;

.container-fluid {
    margin: 0;
    padding: 0;
}

img {
    aspect-ratio: 6 / 3.5;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.primary-button {
    background-color: #262626 !important;

    &:hover {
        background-color: white !important;
        color: $blue !important;
    }
}

.left-bottom {
    min-height: 500px !important;
}

.position-absolute {
    top: 50%;
    transform: translate(0, -50%);

}
</style>