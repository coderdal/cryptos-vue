<template>
  <carousel
    :per-page="1"
    :mouseDrag="true"
    :paginationEnabled="false"
    :loop="true"
    :autoplay="true"
    :autoplayTimeout="5000"
    :centerMode="true"
    @page-change="catchChange"
  >
    <slide>
      <div class="slide">
        <div class="content">
          <h1>
            <span class="orange">SECURE</span> AND
            <span class="orange">EASY WAY</span><br />
            TO BITCOIN
          </h1>
          <button>LEARN MORE</button>
        </div>
        <div class="bg"></div>
        <img src="assets/images/carousel1.jpg" alt="" srcset="" />
      </div>
    </slide>
    <slide>
      <div class="slide">
        <div class="content">
          <h1>
            <span class="orange">BITCOIN</span> EXCHANGE
            <br />
            YOU CAN
            <span class="orange">TRUST</span>
          </h1>
          <button>LEARN MORE</button>
        </div>
        <div class="bg"></div>
        <img src="assets/images/carousel2.jpg" alt="" srcset="" />
      </div>
    </slide>
  </carousel>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "homeCarousel",
  data() {
    return {
      activeSlide: 0,
    };
  },
  components: {
    Carousel,
    Slide,
  },
  methods: {
    catchChange() {
      console.log("changed");
    },
  },
};
</script>

<style scoped>
.slide {
  width: 100%;
  min-height: 70vh;
  max-height: 70vh;
  position: relative;
}

.slide .content {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 99;
  display: flex;
  flex-direction: column;
}

.slide .content h1 {
  padding: 0 30px;
  font-weight: 600;
  text-transform: uppercase;
  font-size: 4em;
  text-align: center;
}

.slide .content h1 .orange {
  color: var(--orange-color);
  font-weight: 700;
}

.slide .content button {
  border: 1px solid var(--orange-color);
  color: var(--orange-color);
  text-transform: uppercase;
  background: transparent;
  margin-top: 15px;
  padding: 12px 24px;
  cursor: pointer;
  font-weight: 600;
  transition: background 350ms ease-in;
}

.slide .content button:hover {
  background: var(--orange-color);
  color: var(--text-light-gray-color);
}

.slide .bg {
  width: 100%;
  min-height: 70vh;
  max-height: 70vh;
  background: rgba(0, 0, 0, 0.4);
  position: absolute;
  top: 0;
  left: 0;
  pointer-events: none;
}

.slide img {
  object-fit: cover;
  width: 100%;
  min-height: 70vh;
  max-height: 70vh;
  pointer-events: none;
}
</style>