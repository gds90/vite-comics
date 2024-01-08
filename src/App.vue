<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppBuyProduct from './components/AppBuyProduct.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppBuyProduct
  }
}
</script>
<template lang="">
  <AppHeader />
  <AppMain />
  <AppBuyProduct/>
  <AppFooter />

</template>
<style lang="scss">
@use './styles/generals.scss'
</style>