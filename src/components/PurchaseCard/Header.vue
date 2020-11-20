<template>
  <div class="header-container row">
    <div class="avatar col-1">
      <img src="../../assets/logo.png" alt="" />
    </div>
    <div class="header-title col-8">
      <h3>Buy a house</h3>
      <h5>Saving goal</h5>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header-container {
  .avatar {
    img {
      height: 5vh;
      width: 5vh;
    }
  }
  .header-title {
    text-align: left;
    margin-left: 10px;
    h3 {
      /* LG / headingSmall */
      font-family: Rubik;
      font-style: normal;
      font-weight: 500;
      font-size: 24px;
      line-height: 120%;
      /* identical to box height, or 29px */

      /* $blueGray900 */
      color: #1e2a32;

      margin: 0px 10px;
    }
    h5 {
      /* LG / paragraph */
      font-family: Work Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 150%;
      /* identical to box height, or 24px */

      /* $blueGray400 */
      color: #708797;

      margin: 0px 10px;
    }
  }
}
</style>
