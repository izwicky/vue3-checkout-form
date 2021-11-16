<template>
  <div>
    <h1 class="p-text-center">{{ $data.ProductName }}</h1>
    <ProductImage />
    <div class="p-text-wrap text-center p-p-4">
      {{ $data.ProductDetails }}
    </div>
  </div>
</template>

<script>
import ProductImage from "./ProductImage.vue";

export default {
  data: () => ({
    ProductName: "Best Coffee - 20oz",
    ProductDetails:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
  }),
  components: {
    ProductImage,
  },
};
</script>

<style scoped></style>
