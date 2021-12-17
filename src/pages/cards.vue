<template>
  <div class="surface">
    <div class="detail__container">
      <!-- Account Container -->
      <div class="account">
        <div class="account__head">
          <h5 class="account__title">Account balance</h5>
          <div>
            <img src="~assets/Logo-green.svg" />
          </div>
        </div>
        <div class="account__balance">
          <div class="account__currency">
            <h6>S$</h6>
            <h2>3,000</h2>
          </div>
          <q-btn flat class="account__add-card-btn" @click="prompt = true">
            <q-icon class="text-dark" size="lg">
              <img src="~assets/Add.svg" />
            </q-icon>
            <h6>New card</h6>
          </q-btn>
        </div>
      </div>

      <!-- Card Container -->
      <q-tabs
        align="justify"
        narrow-indicator
        active-color="white"
        indicator-color="accent"
        class="q-mb-lg text-grey-7 card__tab"
      >
        <q-tab class="q-pa-none" name="My debit cards" label="My debit cards" />
        <q-tab
          class="q-pa-none"
          name="All company cards"
          label="All company cards"
        />
      </q-tabs>

      <q-carousel
        v-model="slide"
        swipeable
        navigation
        animated
        height="100%"
        style="background-color: #0c365a"
      >
        <q-carousel-slide
          v-for="(item, index) in cardList"
          :key="index"
          :name="index"
          class="q-pa-none"
        >
          <div class="card">
            <img class="card__brand" src="~assets/FullLogo.svg" />
            <h2 class="card__name">{{ item.cardName }}</h2>
            <h5 class="card__number">{{ item.cardNumber }}</h5>
            <div class="card__dateCVV">
              <h6 class="card__exp">{{ item.date }}</h6>
              <h6 class="card__cvv">{{ item.cvv }}</h6>
            </div>
            <img class="card__payment-brand" src="~assets/Visa-Logo.svg" />
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>

    <!-- Option Container -->
    <div class="options__container">
      <div class="card__options">
        <div class="card__btn">
          <img src="~assets/Freeze-card.svg" />
          <h6 class="card__btn-text">Freeze card</h6>
        </div>
        <div class="card__btn">
          <img src="~assets/Set-spend-limit.svg" />
          <h6 class="card__btn-text">Set spend limit</h6>
        </div>
        <div class="card__btn">
          <img src="~assets/GPay.svg" />
          <h6 class="card__btn-text">Add to Gpay</h6>
        </div>
        <div class="card__btn">
          <img src="~assets/Replace-card.svg" />
          <h6 class="card__btn-text">Replace card</h6>
        </div>
        <div class="card__btn">
          <img src="~assets/Deactivate-card.svg" />
          <h6 class="card__btn-text">Cancel card</h6>
        </div>
      </div>

      <q-expansion-item
        icon="img:/Card-details.svg"
        expand-icon="img:/down-arrow.svg"
        label="Card details"
        class="expansion"
      >
        <q-card>
          <q-card-section>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quidem,
            eius reprehenderit eos corrupti commodi magni quaerat ex numquam,
            dolorum officiis modi facere maiores architecto suscipit iste
            eveniet doloribus ullam aliquid.
          </q-card-section>
        </q-card>
      </q-expansion-item>

      <q-expansion-item
        icon="img:/Recent-transactions.svg"
        expand-icon="img:/down-arrow.svg"
        label="Recent transactions"
        class="expansion"
      >
        <div>
          <q-list separator>
            <q-item class="expansion--list" clickable>
              <div class="transaction">
                <div class="transaction_details">
                  <div class="transaction__icon">
                    <img src="~assets/file-storage.svg" />
                  </div>
                  <div class="transaction__content">
                    <h5>Hamleys</h5>
                    <h6>20 May 2020</h6>
                    <div class="transaction__status">
                      <div class="transaction__status--icon">
                        <img src="~assets/business-and-finance.svg" />
                      </div>
                      <h6 class="transaction__status--content">
                        Refund on debit card
                      </h6>
                    </div>
                  </div>
                </div>
                <div class="transaction__amount">
                  <h5>+S$ 150</h5>
                  <img src="~assets/next.svg" />
                </div>
              </div>
            </q-item>

            <q-item class="expansion--list" clickable>
              <div class="transaction">
                <div class="transaction_details">
                  <div class="transaction__icon--green">
                    <img src="~assets/flights.svg" />
                  </div>
                  <div class="transaction__content">
                    <h5>Hamleys</h5>
                    <h6>20 May 2020</h6>
                    <div class="transaction__status">
                      <div class="transaction__status--icon">
                        <img src="~assets/business-and-finance.svg" />
                      </div>
                      <h6 class="transaction__status--content">
                        Refund on debit card
                      </h6>
                    </div>
                  </div>
                </div>
                <div class="transaction__amount">
                  <h5>+S$ 150</h5>
                  <img src="~assets/next.svg" />
                </div>
              </div>
            </q-item>

            <q-item class="expansion--list" clickable>
              <div class="transaction">
                <div class="transaction_details">
                  <div class="transaction__icon--pink">
                    <img src="~assets/megaphone.svg" />
                  </div>
                  <div class="transaction__content">
                    <h5>Hamleys</h5>
                    <h6>20 May 2020</h6>
                    <div class="transaction__status">
                      <div class="transaction__status--icon">
                        <img src="~assets/business-and-finance.svg" />
                      </div>
                      <h6 class="transaction__status--content">
                        Refund on debit card
                      </h6>
                    </div>
                  </div>
                </div>
                <div class="transaction__amount">
                  <h5>+S$ 150</h5>
                  <img src="~assets/next.svg" />
                </div>
              </div>
            </q-item>

            <q-item class="expansion--list" clickable>
              <div class="transaction">
                <div class="transaction_details">
                  <div class="transaction__icon">
                    <img src="~assets/file-storage.svg" />
                  </div>
                  <div class="transaction__content">
                    <h5>Hamleys</h5>
                    <h6>20 May 2020</h6>
                    <div class="transaction__status">
                      <div class="transaction__status--icon">
                        <img src="~assets/business-and-finance.svg" />
                      </div>
                      <h6 class="transaction__status--content">
                        Refund on debit card
                      </h6>
                    </div>
                  </div>
                </div>
                <div class="transaction__amount">
                  <h5>+S$ 150</h5>
                  <img src="~assets/next.svg" />
                </div>
              </div>
            </q-item>
          </q-list>

          <div class="all__transaction">
            <h6>View all card transactions</h6>
          </div>
        </div>
      </q-expansion-item>
    </div>

    <q-dialog v-model="prompt" persistent>
      <q-card style="min-width: 350px">
        <q-card-section>
          <div class="text-h6">Enter Your Name On Card</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <q-input
            dense
            v-model="cardName"
            autofocus
            @keyup.enter="prompt = false"
          />
        </q-card-section>

        <q-card-actions align="right" class="text-primary">
          <q-btn flat label="Cancel" v-close-popup />
          <q-btn flat label="Add name" v-close-popup @click="addCard()" />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "Cards",

  setup() {
    return {
      slide: ref(0),
      prompt: ref(false),
      cardName: ref(""),
      cardList: [],
    };
  },

  created() {
    this.init();
  },

  mounted() {},

  methods: {
    init() {
      if (localStorage.getItem("card") === null) {
        let card = [
          {
            cardName: "Mark Henry",
            cardNumber: "0000 0000 0000 2020",
            date: "Thru: 12/20",
            cvv: "CVV: ***",
          },
        ];
        localStorage.setItem("card", JSON.stringify(card));
      }
      this.cardList = JSON.parse(localStorage.getItem("card"));
    },

    addCard() {
      let card = {
        cardName: this.cardName,
        cardNumber: "0000 0000 0000 2020",
        date: "Thru: 12/20",
        cvv: "CVV: ***",
      };
      var existing = JSON.parse(localStorage.getItem("card"));

      existing.push(card);

      localStorage.setItem("card", JSON.stringify(existing));

      setTimeout(() => {
        this.init()
      }, 100);
    },
  },
});
</script>

<style lang="scss">
.surface {
  background-color: $primary;
}
// Transaction Expansion
.expansion {
  margin: 15px;
  background-color: #fafcff;
  border: 1px solid #f5f5f5;
  border-radius: 8px;
  filter: drop-shadow(0 0 8px #0000000a);
  padding: 10px 5px;

  &--list {
    display: block;
    background-color: $white;
    padding: 20px;
  }
}

.transaction {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.transaction_details {
  display: flex;
}

.transaction__icon {
  background-color: #009dff1a;
  display: flex;
  height: 48px;
  width: 48px;
  align-items: center;
  justify-content: center;
  border-radius: 24px;

  &--green {
    @extend .transaction__icon;
    background-color: #00d6b51a;
  }

  &--pink {
    @extend .transaction__icon;
    background-color: #f251951a;
  }
}

.transaction__content {
  margin-left: 15px;
  h5 {
    color: #222222;
    font-weight: 600;
  }
  h6 {
    font-weight: 400;
    color: #aaaaaa;
    margin-top: 5px;
  }
}

.transaction__status {
  display: flex;
  align-items: center;
  margin-top: 10px;
}

.transaction__status--content {
  font-size: 12px;
  font-weight: 600;
  color: #325baf;
  margin-left: 5px;
  margin-top: 0 !important;
}

.transaction__status--icon {
  background-color: #325baf;
  display: flex;
  height: 20px;
  width: 24px;
  align-items: center;
  justify-content: center;
  border-radius: 24px;
}

.transaction__amount {
  display: flex;
  align-items: center;

  h5 {
    color: #01d167;
    font-weight: 700;
    margin-right: 10px;
  }
}

.all__transaction {
  color: #01d167;
  background-color: #edfff5;
  padding: 15px;
  text-align: center;
}

// Card Options
.card__options {
  background-color: #edf3ff;
  border-top-left-radius: 24px;
  border-top-right-radius: 24px;
  display: flex;
  padding: 15px 5px;
}
.card__btn {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.card__btn-text {
  text-align: center;
  margin-top: 7px;
}
// Options
.options__container {
  background-color: $white;
  border-top-left-radius: 24px;
  border-top-right-radius: 24px;
}
// Cards
.detail__container {
  background-color: $primary;
  padding: 20px 30px 0px 30px;
}
.card {
  background-color: $secondary;
  border-radius: 12px;
  margin: 10px 0 50px 0;
  padding: 20px;
  display: flex;
  flex-direction: column;
}
.card__brand {
  align-self: flex-end;
}
.card__name {
  color: $white;
  font-weight: 700;
  letter-spacing: 0.53px;
  margin: 20px 0 10px 0;
}
.card__number {
  color: $white;
  font-weight: 700;
  letter-spacing: 0.53px;
  margin: 10px 0;
}
.card__dateCVV {
  display: flex;
}
.card__exp {
  color: $white;
  font-weight: 700;
  letter-spacing: 0.53px;
  margin-right: 10px;
}
.card__cvv {
  color: $white;
  font-weight: 700;
  letter-spacing: 0.53px;
  margin-left: 10px;
}
.card__payment-brand {
  align-self: flex-end;
}

.card__tab {
  font-size: 13px;
  font-weight: 700;
  margin: 0;
  text-transform: initial;
}
// Account
.account__head {
  display: flex;
  justify-content: space-between;
}
.account__title {
  color: $white;
  font-weight: 600;
}
.account__balance {
  display: flex;
  align-items: center;
  justify-content: space-between;

  h2 {
    line-height: 1.5;
    color: $white;
  }
}
.account__currency {
  display: flex;
  align-items: center;
  h6 {
    background-color: $secondary;
    color: $white;
    font-size: 12px;
    padding: 4px 12px;
    border-radius: 4px;
    line-height: normal;
    margin-right: 10px;
  }
}
.account__add-card-btn {
  color: #23cefd;
  padding: 0;
}
</style>
