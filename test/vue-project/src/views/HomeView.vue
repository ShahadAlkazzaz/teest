<script setup>
import HeroImage from "../components/HeroImage.vue";
import ClothesOffers from "../components/ClothesOffers.vue";
</script>

<template>
  <HeroImage />

 <h1 class="kataloge">{{ message }}</h1>

  <div class="all-kataloge">

    <div class="container text-center">
  <div class="row align-items-start">
    <div class="col">
        <ClothesOffers />
    </div>
  </div>
</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Kataloge",
    };
  },
};
</script>

<style scoped>
.all-kataloge{
    margin-top: 15vh;
}
.kataloge,
h1 {
  display: flex;
  justify-content: center;
  margin-top: 5vh;
  margin-bottom: 30px;
}
</style>
