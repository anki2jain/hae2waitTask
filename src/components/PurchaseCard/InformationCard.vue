<template>
  <div class="information-container">
    <div class="upper-section">
      <h5>Monthly amount</h5>
      <h4 class="ml-auto">$ {{ getMonthlyAmount }}</h4>
    </div>

    <div class="message-section">
      <h6>
        You’re planning <span>{{ months }} monthly deposits</span> to reach your
        <span>$ {{ amount }}</span>
        goal <span> by {{ listOfMonths[getDate()] }} {{ getYear() }}.</span>
      </h6>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    amount: String,
    months: Number,
  },
  data: () => ({
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
  computed: {
    getMonthlyAmount() {
      if (this.amount == "" || this.amount == null) {
        return "NA";
      } else if (this.months == 0) {
        return this.amount;
      }
      return (parseFloat(this.amount) / (this.months + 1)).toFixed(); // rounded off the calculated amount
    },
  },
};
</script>

<style lang="scss" scoped>
.information-container {
  text-align: left;
  margin: 15px 15px;
  background: #ffffff;

  height: fit-content;
  border: 1px solid #e9eef2;
  border-radius: 8px;
  .upper-section {
    display: flex;
    min-height: 80px;

    h5 {
      font-family: Work Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 20px;
      line-height: 120%;
      display: flex;
      align-items: center;

      color: #1e2a32;

      margin: 0px 10px;
    }
    h4 {
      font-family: Rubik;
      font-style: normal;
      font-weight: 500;
      font-size: 32px;
      line-height: 120%;
      display: flex;
      color: #0079ff;
      align-items: center;

      margin: 0px 10px;
    }
  }
  .message-section {
    background: #f4f8fa;
    padding: 20px 20px;
    h6 {
      font-family: Work Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 12px;
      line-height: 16px;
      color: #1e2a32;
      margin: 0px 10px;
    }
    span {
      font-weight: bold;
    }
  }
}
</style>
