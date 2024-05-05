<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import IconsList from './components/IconsList.vue'


export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    IconsList
    
  }
}
</script>

<template>
  

  <AppHeader />
  <IconsList />
  <AppMain />

 
  <AppFooter />
</template>

<style lang="scss">

</style>
