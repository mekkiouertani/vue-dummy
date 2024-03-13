<template>
  <header>
    <TopBar />
    <HeroSlider />
  </header>
  <main>
    <TopSection />
    <MiddleSection />
    <BottomSection />
  </main>
  <footer class="my-bg-dark text-white ">
    <FooterComponent />
  </footer>
</template>

<script>
import TopBar from './components/TopBar.vue';
import HeroSlider from './components/HeroSlider.vue';
import TopSection from './components/main-components/TopSection.vue';
import MiddleSection from './components/main-components/MiddleSection.vue';
import BottomSection from './components/main-components/BottomSection.vue';
import FooterComponent from './components/FooterComponent.vue';
export default {
  name: 'App',
  components: { TopBar, HeroSlider, TopSection, MiddleSection, BottomSection, FooterComponent },
  data() {
    return {

    }
  },

}
</script>

<style lang="scss" scoped></style>