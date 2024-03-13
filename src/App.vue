<template>
  <TopBar />
  <HeroSlider />
</template>

<script>
import TopBar from './components/TopBar.vue';
import HeroSlider from './components/HeroSlider.vue';
export default {
  name: 'App',
  components: { TopBar, HeroSlider },
  data() {
    return {

    }
  },

}
</script>

<style lang="scss" scoped></style>