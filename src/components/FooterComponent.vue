<template>
    <section class="container px-3">
        <FormFooter class="border-bottom" />

        <div class="row align-items-baseline mt-5">
            <div class="col-12 col-lg-4 ">
                <a href="#"><img class="align-middle" src="../images/Logo.svg" alt="logo-nature-agency"></a>
                <a class="navbar-brand fs-3 mx-3 align-middle" href="#"><span class="fw-bold">Nature </span>
                    <span class="fw-light">Agency</span></a>
                <p class="my-4 my-txt-semi-dark">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Perferendis
                    nihil totam eum est
                    officia,
                    commodi quaerat doloremque dolorem doloribus hic ullam ipsa, reprehenderit dolores dignissimos
                    vitae, quasi perspiciatis? Tempore, ipsum?</p>
                <div class="social my-5">
                    <img src="./../../src/images/simple-facebook.svg" alt="social-facebook">
                    <img class="mx-4" src="./../../src/images/simple-instagram.svg" alt="social-instagram">
                    <img src="./../../src/images/simple-linkedin.svg" alt="social-linkedin">
                </div>
            </div>
            <div class="col-12 col-lg-8 d-flex flex-wrap  justify-content-around">
                <ul v-for="el in list" class="no-list-style ">
                    <li class="text-primary mb-3 fw-bold">{{ el.title }}</li>
                    <li class="mb-1" v-for="items in el.items">{{ items }}</li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
import FormFooter from "./../components/FormFooter.vue";
export default {
    components: { FormFooter },
    name: 'FooterComponent',
    data() {
        return {
            list: [
                {
                    title: 'Contact',
                    items: [
                        'Message',
                        'Email',
                        'Phone',
                        'Address'
                    ]
                },
                {
                    title: 'Reviews',
                    items: [
                        'Feedback',
                        'Rating',
                        'Testimonials',
                        'User Experiences'
                    ]
                },
                {
                    title: 'Services',
                    items: [
                        'Development',
                        'Design',
                        'Marketing',
                        'SEO',
                        'Support'
                    ]
                },
                {
                    title: 'Team',
                    items: [
                        'Management',
                        'Sales',
                        'Development',
                        'Design',
                        'Marketing'
                    ]
                }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.container {
    padding: 50px 0;
}

ul {
    list-style: none;
}
</style>