<template>
  <div id="card-details">
    <h6 class="text-end text-secondary">
      <b
        ><img
          src="@/assets/remove_red_eye-24px.png"
          class="v-align-middle"
        />Show card number</b
      >
    </h6>
    <div class="card">
      <div class="text-end">
        <img src="@/assets/AspireLogo.png" id="logo" />
      </div>
      <div id="name" class="text-start">Mark Henry</div>
      <div id="card-number" class="text-start">
        <span class="dot" v-for="index in 4" :key="index">&#8226;</span>
        <span class="space"></span>
        <span class="dot" v-for="index in 4" :key="index">&#8226;</span>
        <span class="space"></span>
        <span class="dot" v-for="index in 4" :key="index">&#8226;</span>
        <span class="space"></span>
        <span class="number"><b>2021</b></span>
      </div>
      <div id="expiry-csv">
        <div id="expiry">
          <b>Thru : 12/21</b>
        </div>
        <div id="cvv">
          <b>CVV : ***</b>
        </div>
      </div>
      <div id="visa-logo" class="text-end">
        <img src="@/assets/VisaLogo.png" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Card",
};
</script>
<style lang="scss" scoped>
.card {
  background-color: $secondary-color;
  border-radius: 10px;
  margin-top: 0.5rem;
  #logo {
    margin-top: 2rem;
    margin-right: 2rem;
  }
  #name {
    font-size: 24px;
    font-weight: bold;
    margin-top: 2rem;
    margin-left: 2rem;
    color: white;
  }
  #card-number {
    margin-top: 0.5rem;
    margin-left: 2rem;
    color: white;
    display: flex;
    align-items: center;
    .space {
      margin-right: 1rem;
    }
    .dot {
      font-size: 36px;
    }
  }
  #expiry-csv {
    display: flex;
    margin-left: 2rem;
    margin-top: 0.5rem;
    gap: 2rem;
    div > b {
      color: white;
    }
  }
  #visa-logo {
    margin-right: 2rem;
    margin-bottom: 2rem;
    img {
      margin-bottom: 1rem;
    }
  }
}
</style>
