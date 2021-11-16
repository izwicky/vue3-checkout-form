<template>
  <Image :src="coffee" alt="Coffee 100% Rexy" width="250" />
</template>

<script>
import Image from "primevue/image";
import coffee from "@/assets/img/coffee.jpg";

export default {
  components: {
    Image,
  },
  data: () => ({
    coffee: coffee,
  }),
};
</script>

<style scoped></style>
