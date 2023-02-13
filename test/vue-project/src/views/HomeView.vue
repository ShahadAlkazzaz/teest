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
        <clothe-offers
          v-for="clothe in clothes"
          :key="clothe.id"
          :sale="clothe"
          :img="image"
        />
        <!-- <ClothesOffers /> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Kataloge",
      clothes: [],
    };
  },

  components: { "clothe-offers": ClothesOffers },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const res = await fetch("baby.json");
      const result = await res.json();
      this.clothes = result;
    },
  },
};
</script>

<style scoped>
.all-kataloge {
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
