<template>
  <section class="about">
    <div class="titles">
      <h2 class="title">about <span class="orange">us</span></h2>
      <p class="introduction-title">
        A COMMERCIAL WEBSITE THAT LISTS WALLETS, EXCHANGES AND OTHER BITCOIN
        RELATED INFO
      </p>
    </div>

    <div class="content">
      <div class="about-us">
        <figure>
          <img src="assets/images/about-us.png" alt="About Us Logo" />
        </figure>
        <div class="text-content">
          <h2>We Are ERDALCOİN</h2>
          <p>
            A place for everyone who wants to simply buy and sell Bitcoins.
            Deposit funds using your Visa/MasterCard or bank transfer. Instant
            buy/sell of Bitcoins at fair price is guaranteed. Nothing extra.
            Join over 700,000 users from all over the world satisfied with our
            services.
          </p>
          <div class="text-buttons">
            <p
              @click="activeText = textArray[0]"
              :class="{ active: activeText === textArray[0] }"
            >
              Our Mission
            </p>
            <span class="divide-line"></span>
            <p
              @click="activeText = textArray[1]"
              :class="{ active: activeText === textArray[1] }"
            >
              Our Advantages
            </p>
            <span class="divide-line"></span>
            <p
              @click="activeText = textArray[2]"
              :class="{ active: activeText === textArray[2] }"
            >
              Our guarantees
            </p>
          </div>
          <p class="active-text">{{ activeText }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "homeAbout",
  data() {
    return {
      textArray: [
        "Bitcoin is based on a protocol known as the blockchain, which allows to create, transfer and verify ultra-secure financial data without interference of third parties.",
        "Our mission as an official partner of Bitcoin Foundation is to help you enter and better understand the world of #1 cryptocurrency and avoid any issues you may encounter.",
        "We are here because we are passionate about open, transparent markets and aim to be a major driving force in widespread adoption, we are the first and the best in cryptocurrency.",
      ],
      activeText:
        "Bitcoin is based on a protocol known as the blockchain, which allows to create, transfer and verify ultra-secure financial data without interference of third parties.",
    };
  },
};
</script>

<style scoped>
.about {
  margin-top: 220px;
}

/* Titles */

.about .titles {
  text-align: center;
}

.about .titles .title {
  text-transform: uppercase;
  font-size: 2.6em;
}

.about .titles .introduction-title {
  text-transform: uppercase;
  text-align: center;
  margin-top: 12px;
  color: var(--text-lighter-color);
  font-size: 0.9em;
  position: relative;
  display: inline-block;
}

.about .titles .introduction-title::before {
  content: "";
  position: absolute;
  height: 2px;
  right: -40px;
  top: 50%;
  width: 30px;
  background: var(--orange-color);
}

.about .titles .introduction-title::after {
  content: "";
  position: absolute;
  height: 2px;
  left: -40px;
  top: 50%;
  width: 30px;
  background: var(--orange-color);
}

/* Content */

.about .content {
  width: 100%;
}

.about .content .about-us {
  text-align: center;
  width: 82%;
  max-width: 1170px;
  margin: 30px auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 30px;
}

.about .content .about-us .text-content {
  text-align: left;
  padding-right: 10px;
  padding-left: 30px;
}

.about .content .about-us .text-content h2 {
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.6em;
}

.about .content .about-us .text-content > p {
  color: var(--text-lighter-color);
  margin-top: 10px;
}

.about .content .about-us .text-content .text-buttons {
  width: 100%;
  display: flex;
  gap: 20px;
  justify-content: space-between;
  margin-top: 22px;
}

.about .content .about-us .text-content .text-buttons p {
  text-transform: uppercase;
  color: var(--text-lighter-color);
  cursor: pointer;
}

.about .content .about-us .text-content .text-buttons p.active {
  color: var(--orange-color);
  font-weight: 600;
}

.about .content .about-us .text-content .text-buttons .divide-line {
  width: 1px;
  height: 26px;
  background: var(--text-lighter-color);
}

.about .content .about-us .text-content .active-text {
  margin-top: 16px;
}

/* Media Queries */

@media screen and (max-width: 1140px) {
  .about .content .about-us .text-content .text-buttons .divide-line {
    height: 44px;
  }
}

@media screen and (max-width: 915px) {
  .about .content .about-us {
    flex-direction: column;
  }
  .about .content .about-us .text-content .text-buttons .divide-line {
    height: 26px;
  }
}
</style>