<template>
  <div class="container">
    <side-nav />
    <div id="main">
      <div id="content"><router-view /></div>
    </div>
  </div>
</template>
<script>
import SideNav from "@/components/SideNav";
export default {
  name: "App",
  components: { SideNav },
};
</script>
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
    max-height: 100vh !important;
    overflow: auto;
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
