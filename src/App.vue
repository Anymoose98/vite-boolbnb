<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from "./components/AppFooter.vue";
import AppMain from "./components/AppMain.vue";
export default {
  components: {
    AppHeader,
    AppFooter,
    AppMain,
  }
}
</script>


<template lang="">
  <AppHeader />
  <AppMain />
  <!-- <router-view></router-view> -->
  <AppFooter />
</template>
<style lang="scss">
</style>