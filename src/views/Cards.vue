<template>
  <div class="content">
    <div id="top-bar">
      <div id="available-balance">
        <div><b>Available balance</b></div>
        <br />
        <div class="d-flex align-items-center">
          <div class="dollar"><span>S$</span></div>
          <h2>3,000</h2>
        </div>
      </div>
      <div id="new-card">
        <button><img src="@/assets/box.png" />New card</button>
      </div>
    </div>
    <div id="details">
      <div class="d-flex gap-1 tabs">
        <div class="active"><b>My debit cards</b></div>
        <div class="o-30">All company cards</div>
      </div>
      <div id="transaction-details">
        <div id="card-n-limits">
          <Card />
          <Actions />
        </div>
        <div id="details-n-transactions">
          <div id="card-details-accordion" class="accordion">
            <div class="d-flex justify-content-center align-items-center gap-1">
              <img src="@/assets/Group.png" />Card details
            </div>
            <div><img src="@/assets/down-arrow.png" alt="" /></div>
          </div>
          <div class="accordion" id="recent-transactions-accordion">
            <div class="d-flex justify-content-center align-items-center gap-1">
              <img src="@/assets/Group11889.png" />Recent Transactions
            </div>
            <div><img src="@/assets/up-arrow.png" alt="" /></div>
          </div>
          <div class="transaction-holder">
            <span v-for="transaction in transactions" :key="transaction">
              <Transaction :transaction="transaction" />
            </span>
          </div>
          <div id="footer">View all card transactions</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Card from "@/components/Card";
import Actions from "@/components/Actions";
import Transaction from "@/components/Transaction";
export default {
  name: "Cards",
  components: { Card, Actions, Transaction },
  created() {
    this.transactions = [];
    this.transactions.push({
      icon: "file-storage",
      name: "Hamleys",
      date: "20 May 2020",
      description: "Refund to debit card",
      type: "earnt",
    });
    this.transactions.push({
      icon: "flights",
      name: "Hamleys",
      date: "20 May 2020",
      description: "Charged on debit card",
      type: "spent",
    });
    this.transactions.push({
      icon: "megaphone",
      name: "Hamleys",
      date: "20 May 2020",
      description: "Charged on debit card",
      type: "spent",
    });
    this.transactions.push({
      icon: "file-storage",
      name: "Hamleys",
      date: "20 May 2020",
      description: "Charged on debit card",
      type: "spent",
    });
  },
  data() {
    return {
      transactions: [],
    };
  },
};
</script>

<style scoped lang="scss">
#top-bar {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  #new-card > button {
    @include center-item;
    background-color: $blue-variant;
    color: white;
    border: none;
    border-radius: 5px;
    padding: 8px 12px;
    cursor: pointer;
    img {
      margin-right: 5px;
    }
  }
}

.dollar {
  width: 40px;
  height: 24px;
  border-radius: 5px;
  background-color: $secondary-color;
  color: #ffffff;
  font-size: 12px;
  font-weight: bold;
  margin-right: 0.5rem;
  @include center-item;
}

#details {
  margin-top: 3rem;
  .tabs {
    div {
      padding: 5px 0px;
    }
    .active {
      position: relative;
      b {
        &::after {
          content: "";
          position: absolute;
          width: 100%;
          height: 2px;
          background-color: $underline-color;
          bottom: 0;
          left: 0;
        }
      }
    }
  }
  #transaction-details {
    padding: 2rem;
    margin-top: 2rem;
    border-radius: 10px;
    border: 1px solid #fcfcfc;
    box-shadow: 0px 2px 12px #00000014;
    display: flex;
    gap: 3rem;
    #card-n-limits {
      flex-basis: 45%;
    }
    #details-n-transactions {
      flex-basis: 55%;
      .transaction-holder {
        border: 1px solid #f0f0f0;
      }
      #footer {
        padding: 1rem;
        color: $secondary-color;
        background-color: #edfff5;
        font-weight: bold;
        border: 1px solid #fcfcfc;
      }
    }
    .accordion {
      padding: 2rem;
      background-color: $transparent-background;
      margin-top: 2rem;
      border-radius: 10px;
      box-shadow: 0px 0px 8px #0000000a;
      @include center-item;
      justify-content: space-between !important;
    }
  }
}
</style>
