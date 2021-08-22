<template>
  <div id="actions">
    <div class="action">
      <div><img src="@/assets/Freezecard.png" /></div>
      Freeze<br />
      Card
    </div>
    <div class="action">
      <div><img src="@/assets/Setspendlimit.png" /></div>
      Set spend <br />
      limit
    </div>
    <div class="action">
      <div><img src="@/assets/GPay.png" /></div>
      Add to <br />
      Gpay
    </div>
    <div class="action">
      <div><img src="@/assets/Replacecard.png" /></div>
      Replace <br />
      card
    </div>
    <div class="action">
      <div><img src="@/assets/Deactivatecard.png" /></div>
      Cancel <br />
      card
    </div>
  </div>
</template>
<script>
export default {
  name: "Actions",
};
</script>
<style lang="scss" scoped>
#actions {
  padding: 2rem;
  background-color: $transparent-background;
  @include center-item;
  justify-content: space-evenly !important;
  gap: 1.5rem;
  .action {
    cursor: pointer;
    font-size: 12px;
  }
}
</style>
