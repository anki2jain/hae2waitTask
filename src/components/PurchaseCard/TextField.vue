<template>
  <div class="textfield-container row">
    <div class="amount-field col-md-6">
      <h6>Total Amount</h6>

      <div class=" container text-box">
        <h5>$</h5>
        <!--  <h4>2500</h4> -->
        <input
          type="number"
          v-model="amount"
          @change="$emit('amount-update', amount)"
        />
      </div>
    </div>

    <div class="date-field col-md-6">
      <h6>Reach Goal by</h6>

      <div class=" container text-box">
        <img
          src="../../assets/arrow_right.png"
          alt=""
          srcset=""
          v-bind:style="months ? 'cursor:pointer;' : 'cursor: not-allowed;'"
          @click="decreaseMonths()"
        />

        <h6 class="m-auto text-center">
          {{ listOfMonths[getDate()] }}
          <br />{{ getYear() }}
        </h6>
        <img
          src="../../assets/arrow_left.png"
          alt=""
          srcset=""
          style="cursor:pointer"
          @click="increaseMonths()"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    amount: "",
    months: 0,
    listOfMonths: [
      "January",
      "February",
      "March",
      "April",
      "May",
      "June",
      "July",
      "August",
      "September",
      "October",
      "November",
      "December",
    ],
  }),

  methods: {
    decreaseMonths() {
      if (this.months) this.months--;
      this.$emit("month-update", this.months);
    },
    increaseMonths() {
      this.months++;
      this.$emit("month-update", this.months);
    },

    getDate() {
      let date = new Date();
      var newDate = new Date(date.setMonth(date.getMonth() + this.months));
      return newDate.getMonth();
    },

    getYear() {
      let date = new Date();
      var newDate = new Date(date.setMonth(date.getMonth() + this.months));
      return newDate.getFullYear();
    },
  },
};
</script>

<style lang="scss" scoped>
input {
  border-width: 0px;
  border: none;
  width: fit-content;
}
input:focus {
  outline: none;
}
.textfield-container {
  margin: 20px 0px;
  align-items: center;

  text-align: left;
  h6 {
    margin-top: 10px;
    font-family: Work Sans;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 150%;
    color: #1e2a32;
  }
  .text-box {
    display: flex;
    align-items: center;
    height: 50px;
    background: #ffffff;
    border: 1px solid #e9eef2;
    box-sizing: border-box;
    border-radius: 4px;
    h4 {
      margin-left: 10px;
      font-family: Rubik;
      font-style: normal;
      font-weight: 500;
      font-size: 24px;
      line-height: 120%;

      color: #4d6475;
    }
    h5 {
      color: #708797;
    }
  }

  //   .amount-field {
  //   }
}
</style>
