<template>
  <li>
    <router-link :to="to" active-class="active" exact
      ><slot />

      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="#fff"
        v-if="search"
      >
        <path
          d="M23.822 20.88l-6.353-6.354c.93-1.465 1.467-3.2 1.467-5.059.001-5.219-4.247-9.467-9.468-9.467s-9.468 4.248-9.468 9.468c0 5.221 4.247 9.469 9.468 9.469 1.768 0 3.421-.487 4.839-1.333l6.396 6.396 3.119-3.12zm-20.294-11.412c0-3.273 2.665-5.938 5.939-5.938 3.275 0 5.94 2.664 5.94 5.938 0 3.275-2.665 5.939-5.94 5.939-3.274 0-5.939-2.664-5.939-5.939z"
        />
      </svg>

      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="#fff"
        v-if="cart"
      >
        <path
          d="M10 20.5c0 .829-.672 1.5-1.5 1.5s-1.5-.671-1.5-1.5c0-.828.672-1.5 1.5-1.5s1.5.672 1.5 1.5zm3.5-1.5c-.828 0-1.5.671-1.5 1.5s.672 1.5 1.5 1.5 1.5-.671 1.5-1.5c0-.828-.672-1.5-1.5-1.5zm6.304-17l-3.431 14h-2.102l2.541-11h-16.812l4.615 13h13.239l3.474-14h2.178l.494-2h-4.196z"
        />
      </svg>
    </router-link>
  </li>
</template>

<script>
export default {
  name: "navigationLink",
  props: {
    to: {
      type: String,
      default: "/",
    },
    cart: {
      type: Boolean,
      default: false,
    },
    search: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
header .header-bottom nav ul li a {
  text-decoration: none;
  text-transform: uppercase;
  color: var(--text-color);
  font-weight: 600;
  font-size: 0.9em;
  transition: 200ms all ease-in;
}

header .header-bottom nav ul li a:hover {
  color: var(--orange-color);
}

header .header-bottom nav ul li a.active {
  color: var(--orange-color);
}

header .header-bottom nav ul li a.active svg {
  fill: var(--orange-color);
}

header .header-bottom nav ul li a svg {
  width: 20px;
  height: 20px;
}
</style>