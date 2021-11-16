<template>
  <div
    class="p-grid app-container p-lg-offset-2 p-md-offset-2 p-shadow-6 p-mt-6"
  >
    <div class="p-col-12 p-md-4 p-lg-4 info-container-bg">
      <InfoContainer />
    </div>
    <div class="p-col-12 p-md-8 p-lg-8">
      <CheckoutContainer />
    </div>
  </div>
</template>

<script>
import CheckoutContainer from "./components/checkout-section/CheckoutContainer.vue";
import InfoContainer from "./components/info-section/InfoContainer.vue";

export default {
  name: "App",
  components: {
    CheckoutContainer,
    InfoContainer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Nunito");
body {
  background-color: #9fa8da;
  font-family: Nunito;
}
.app-container {
  background-color: #ffffff;
  width: 60%;
}
.info-container-bg {
  background-color: #eceff1;
}
</style>
