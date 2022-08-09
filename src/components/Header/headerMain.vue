<template>
  <header>
    <header-top />
    <header-bottom />
  </header>
</template>

<script>
import headerTop from "@/components/Header/headerTop.vue";
import HeaderBottom from "./headerBottom.vue";

export default {
  name: "headerMain",
  components: {
    headerTop,
    HeaderBottom,
  },
};
</script>

<style scoped>
header {
  width: 100%;
  height: 140px;
  background: var(--container-bg-color);
  position: relative;
}
</style>