<template>
  <div class="home ">
    <navigation-bar></navigation-bar>
    <div class="title">Let's plan your saving goal.</div>
    <PurchaseCard class="m-auto"></PurchaseCard>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import NavigationBar from "@/components/NavigationBar/NavigationBar";
// import PurchaseCard from "@/components/PurchaseCard/PurchaseCard";
import PurchaseCard from "@/components/PurchaseCard/Index.vue";
export default {
  name: "Home",
  components: {
    HelloWorld,
    NavigationBar,
    PurchaseCard,
  },
};
</script>

<style lang="scss">
.home {
  background: #f4f8fa;

  align-items: center;
  height: 100vh;

  .title {
    padding: 2vh 0px;
    position: static;
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 120%;
    text-align: center;

    color: #1b31a8;
  }
}
</style>
