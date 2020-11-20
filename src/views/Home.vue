<template>
  <div class="home ">
    <navigation-bar></navigation-bar>
    <div class="title">Let's plan your saving goal.</div>
    <PurchaseCard class="offset-md-4"></PurchaseCard>
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
  background: #e5e5e5;
  height: 100vh;

  .title {
    padding: 2vh 0px;
    position: static;
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 120%;
    text-align: center;

    /* $brandColorPrimary */
    color: #1b31a8;

    /* Inside Auto Layout */
    flex: none;
    order: 0;
    align-self: stretch;
    flex-grow: 0;
    margin: 0px 10px;
  }
}
</style>
