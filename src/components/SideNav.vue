<template>
  <div id="sidenav">
    <div class="text-start">
      <img src="@/assets/Logo.png" />
    </div>
    <div class="text-start" id="company-description">
      Trusted way of banking for 3,000+ SMEs and startups in Singapore
    </div>
    <div id="nav-items">
      <div class="nav-item"><img src="@/assets/Home.png" />Home</div>
      <div class="nav-item active"><img src="@/assets/Card.png" />Cards</div>
      <div class="nav-item"><img src="@/assets/Payments.png" />Payments</div>
      <div class="nav-item"><img src="@/assets/Credit.png" />Credit</div>
      <div class="nav-item"><img src="@/assets/Account.png" />Settings</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideNav",
};
</script>

<style scoped lang="scss">
#sidenav {
  background-color: $primary-color;
  flex-basis: 25%;
  padding: 3rem;
  #company-description {
    color: #ffffff;
    opacity: 0.3;
    margin-top: 1rem;
  }
  #nav-items {
    margin-top: 4rem;
    .nav-item {
      cursor: pointer;
      color: white;
      text-align: start;
      font-size: 16px;
      padding: 1.5rem 0px;
      display: flex;
      align-items: center;
      gap: 1rem;
      &.active {
        color: $secondary-color;
      }
    }
  }
}
</style>
