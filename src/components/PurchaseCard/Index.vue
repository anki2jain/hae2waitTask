<template>
  <div class="purchase-card text-center">
    <Header></Header>
    <TextField
      @amount-update="amountUpdate"
      @month-update="monthUpdate"
    ></TextField>
    <InformationCard :amount="amount" :months="totalMonths"></InformationCard>
    <Button class="mt-auto"></Button>
  </div>
</template>

<script>
import Button from "@/components/PurchaseCard/Button";
import Header from "@/components/PurchaseCard/Header";
import TextField from "@/components/PurchaseCard/TextField";
import InformationCard from "@/components/PurchaseCard/InformationCard";
export default {
  components: {
    Button,
    Header,
    TextField,
    InformationCard,
  },

  data: () => ({
    amount: "",
    totalMonths: 0,
  }),

  methods: {
    amountUpdate(val) {
      this.amount = val;
    },
    monthUpdate(val) {
      this.totalMonths = val;
    },
  },
};
</script>
<style lang="scss">
.purchase-card {
  background: white;

  height: fit-content;
  width: fit-content;
  padding: 25px 40px;
  background: #ffffff;
  box-shadow: 0px 16px 32px rgba(30, 42, 50, 0.08);
  border-radius: 8px;
}
</style>
