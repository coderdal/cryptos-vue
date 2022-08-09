<template>
  <div id="app">
    <header-main />
    <home-main />
  </div>
</template>

<script>
import homeMain from '@/components/Home/homeMain.vue';
import headerMain from '@/components/Header/headerMain.vue';

export default {
  name: "App",
  components: {
    homeMain,
    headerMain
  }  
}
</script>

<style scoped>
</style>
