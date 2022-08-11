<template>
  <section>
    <div class="content">
      <div class="info-box">
        <img src="assets/images/wallet-icon.png" alt="Wallet Icon" />
        <div class="text">
          <h2>Download Bitcoin Wallet</h2>
          <p>Get it on PC or Mobile to create, send and receive bitcoins.</p>
        </div>
      </div>
      <div class="info-box">
        <img src="assets/images/cash-icon.png" alt="Wallet Icon" />
        <div class="text">
          <h2>Add coins to your Wallet</h2>
          <p>Add bitcoins you’ve created or exchanged via credit card.</p>
        </div>
      </div>
      <div class="info-box">
        <img src="assets/images/exchange-icon.png" alt="Wallet Icon" />
        <div class="text">
          <h2>Buy/Sell with Wallet</h2>
          <p>Enter receiver's address, specify the amount and send.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "homeShortInfo",
};
</script>

<style scoped>
section {
  position: absolute;
  width: 100%;
  margin: -40px auto;
  z-index: 5;
}

section .content {
  background: var(--container-bg-color);
  width: 82%;
  max-width: 1170px;
  padding: 60px 50px 50px 50px;
  border-radius: 2px;
  margin: 0 auto;
  display: flex;
}

section .content .info-box {
  display: flex;
}

section .content .info-box img {
  width: 50px;
  height: 50px;
}

section .content .info-box .text {
  padding: 0px 10px;
  margin-left: 15px;
  margin-right: 10px;
}

section .content .info-box .text h2 {
  font-size: 1.2em;
  font-weight: 600;
}

section .content .info-box .text p {
  color: var(--text-grayish-color);
  margin-top: 5px;
  font-size: 0.9em;
}
</style>