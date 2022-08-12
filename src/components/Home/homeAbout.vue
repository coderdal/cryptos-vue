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
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "homeAbout",
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
}

.about .content .about-us .text-content h2 {
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.6em;
}

.about .content .about-us .text-content p {
  color: var(--text-lighter-color);
  margin-top: 10px;
}
</style>