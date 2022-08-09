<template>
  <section class="header-bottom" ref="stickyNavigation">
    <nav>
      <ul>
        <navigation-link to="/">Home</navigation-link>
        <navigation-link to="/about">ABOUT US</navigation-link>
        <navigation-link to="/services">SERVICES</navigation-link>
        <navigation-link to="/pricing">PRICING</navigation-link>
        <navigation-link to="/blog">BLOG</navigation-link>
        <navigation-link to="/contact">CONTACT</navigation-link>

        <navigation-link to="/cart" :cart="true" />
        <navigation-link to="/search" :search="true" />
      </ul>
    </nav>
  </section>
</template>

<script>
import navigationLink from "./navigationLink.vue";

export default {
  name: "headerBottom",
  components: { navigationLink },
  created() {
    window.addEventListener("scroll", () => {
      if (window.scrollY > 90) {
        this.$refs.stickyNavigation.style.position = "fixed";
      } else {
        this.$refs.stickyNavigation.style.position = "relative";
      }
    });
  },
};
</script>

<style scoped>
header .header-bottom {
  height: 50px;
  width: 100%;
  z-index: 100;
  background: var(--body-bg-color);
  border-bottom: 1px solid var(--border-color);
  position: relative;
  top: 0;
  left: 0;
}

header .header-bottom nav {
  width: 100%;
  height: 100%;
}

header .header-bottom nav ul {
  width: 100%;
  height: 100%;
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 35px;
}
</style>