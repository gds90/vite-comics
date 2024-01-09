<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppBuyProduct from './components/AppBuyProduct.vue';
import AppJumbotron from './components/AppJumbotron.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppBuyProduct,
    AppJumbotron
  }
}
</script>
<template lang="">
  <AppHeader />
  <AppJumbotron />
  <AppMain />
  <AppBuyProduct/>
  <AppFooter />

</template>
<style lang="scss">
@use './styles/generals.scss'
</style>