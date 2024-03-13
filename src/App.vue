<template>
  <TopBar />
  <HeroSlider />
  <main>
    <TopSection />
    <MiddleSection />
  </main>
</template>

<script>
import TopBar from './components/TopBar.vue';
import HeroSlider from './components/HeroSlider.vue';
import TopSection from './components/main-components/TopSection.vue';
import MiddleSection from './components/main-components/MiddleSection.vue';
export default {
  name: 'App',
  components: { TopBar, HeroSlider, TopSection, MiddleSection },
  data() {
    return {

    }
  },

}
</script>

<style lang="scss" scoped></style>