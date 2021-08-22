<template>
  <div class="container">
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
    <div id="main">
      <div id="content"><router-view /></div>
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.container {
  display: flex;
  > div {
    min-height: 100vh !important;
    overflow: auto;
  }
}
#sidenav {
  background-color: $primary-color;
  flex-basis: 25%;
  padding: 3rem;
  #company-description {
    color: #ffffff;
    opacity: 30%;
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
#main {
  flex-basis: 75%;
  #content {
    margin: 60px auto;
    overflow: scroll;
    min-height: 100%;
  }
}
</style>
