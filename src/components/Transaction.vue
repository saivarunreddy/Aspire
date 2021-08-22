<template>
  <div class="transaction">
    <div class="d-flex gap-1">
      <div class="img-div">
        <img :src="require(`@/assets/${transaction.icon}.png`)" alt="" />
      </div>
      <div>
        <div class="text-start">
          <b>{{ transaction.name }}</b>
        </div>
        <div class="text-start text-light">{{ transaction.date }}</div>
        <div class="charge-text">
          <div class="b-n-f">
            <img src="@/assets/business-and-finance.png" />
          </div>
          <b class="text-primary">{{ transaction.description }}</b>
        </div>
      </div>
    </div>
    <div class="amount" :class="transaction.type">
      <template v-if="transaction.type === 'earnt'">+</template
      ><template v-else>-</template> S$ 150
      <img src="@/assets/next.png" alt="" />
    </div>
  </div>
</template>
<script>
export default {
  name: "Transaction",
  props: ["transaction"],
};
</script>
<style lang="scss" scoped>
.transaction {
  position: relative;
  @include center-item;
  justify-content: space-between;
  padding: 2rem;
  .img-div {
    width: 48px;
    height: 48px;
    border-radius: 50%;
    background-color: #009dff1a;
    @include center-item;
  }
  .amount {
    font-weight: bold;
    &.earnt {
      color: $secondary-color;
    }
    img {
      margin-left: 0.5rem;
    }
  }
  .charge-text {
    @include center-item;
    gap: 0.5rem;
    margin-top: 0.5rem;
    div {
      width: 24px;
      height: 20px;
      background-color: #325baf;
      border-radius: 50%;
    }
  }
  &:not(:last-child):after {
    content: "";
    position: absolute;
    width: 100%;
    height: 2px;
    background-color: #aaaaaa20;
    bottom: 2px;
    left: 0;
  }
}
</style>
