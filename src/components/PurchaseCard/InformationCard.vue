<template>
  <div class="information-container">
    <div class="upper-section">
      <h5>Monthly amount</h5>
      <h4 class="ml-auto">
        $ 541
      </h4>
    </div>

    <div class="message-section">
      <h6>
        You’re planning <span>48 monthly deposits</span> to reach your
        <span>$25,000</span>
        goal <span> by October 2020.</span>
      </h6>
    </div>
  </div>
</template>

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
    padding: 20px 0px;
    h6 {
      position: static;
      left: 0%;
      right: 0%;
      top: 0%;
      bottom: 0%;

      /* caption */
      font-family: Work Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 12px;
      line-height: 16px;
      /* or 133% */

      /* $blueGray900 */
      color: #1e2a32;

      /* Inside Auto Layout */
      flex: none;
      order: 0;
      align-self: stretch;
      flex-grow: 0;
      margin: 0px 10px;
    }
  }
}
</style>
