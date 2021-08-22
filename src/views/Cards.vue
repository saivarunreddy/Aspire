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
                  <b>Thru : 12/20</b>
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
            <div class="transaction">
              <div class="d-flex gap-1">
                <div class="img-div">
                  <img src="@/assets/file-storage.png" alt="" />
                </div>
                <div>
                  <div class="text-start"><b>Hamleys</b></div>
                  <div class="text-start text-light">20 May 2020</div>
                  <div class="charge-text">
                    <div class="b-n-f">
                      <img src="@/assets/business-and-finance.png" />
                    </div>
                    <b class="text-primary">Refund on debit card</b>
                  </div>
                </div>
              </div>
              <div class="amount earnt">
                + S$ 150 <img src="@/assets/next.png" alt="" />
              </div>
            </div>
            <div class="transaction">
              <div class="d-flex gap-1">
                <div class="img-div">
                  <img src="@/assets/flights.png" alt="" />
                </div>
                <div>
                  <div class="text-start"><b>Hamleys</b></div>
                  <div class="text-start text-light">20 May 2020</div>
                  <div class="charge-text">
                    <div class="b-n-f">
                      <img src="@/assets/business-and-finance.png" />
                    </div>
                    <b class="text-primary">Charged to debit card</b>
                  </div>
                </div>
              </div>
              <div class="amount spent">
                - S$ 150 <img src="@/assets/next.png" alt="" />
              </div>
            </div>
            <div class="transaction">
              <div class="d-flex gap-1">
                <div class="img-div">
                  <img src="@/assets/megaphone.png" alt="" />
                </div>
                <div>
                  <div class="text-start"><b>Hamleys</b></div>
                  <div class="text-start text-light">20 May 2020</div>
                  <div class="charge-text">
                    <div class="b-n-f">
                      <img src="@/assets/business-and-finance.png" />
                    </div>
                    <b class="text-primary">Charged to debit card</b>
                  </div>
                </div>
              </div>
              <div class="amount spent">
                - S$ 150 <img src="@/assets/next.png" alt="" />
              </div>
            </div>
            <div class="transaction">
              <div class="d-flex gap-1">
                <div class="img-div">
                  <img src="@/assets/file-storage.png" alt="" />
                </div>
                <div>
                  <div class="text-start"><b>Hamleys</b></div>
                  <div class="text-start text-light">20 May 2020</div>
                  <div class="charge-text">
                    <div class="b-n-f">
                      <img src="@/assets/business-and-finance.png" />
                    </div>
                    <b class="text-primary">Charged to debit card</b>
                  </div>
                </div>
              </div>
              <div class="amount spent">
                - S$ 150 <img src="@/assets/next.png" alt="" />
              </div>
            </div>
          </div>
          <div id="footer">View all card transactions</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Cards",
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
      }
      #footer {
        padding: 1rem;
        color: $secondary-color;
        background-color: #edfff5;
        font-weight: bold;
        border: 1px solid #fcfcfc;
      }
    }
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
