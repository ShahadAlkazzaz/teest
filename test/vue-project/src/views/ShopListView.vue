<script setup>
import ToDoList from "../components/ToShopList.vue";
</script>

<template>
  <div class="container-title">
    <h1 class="title-text">{{ message }}</h1>
  </div>
  <ToDoList />
</template>

<script scoped>
export default {
  data() {
    return {
      message: "Shop List",
    };
  },
};
</script>
<style scoped>
.container-title {
  display: flex;
  justify-content: center;
  margin-top: 5vh;
}

.title-text {
  animation-name: example;
  animation-duration: 5s;
  animation-iteration-count: 30;
  height: 60px;
  width: 180px;
  border: 10px;
  border-radius: 10px;
}

@keyframes example {
  0% {
    background-color: rgb(233, 143, 192);
  }
  25% {
    background-color:rgb(227, 107, 173);
  }
  50% {
    background-color: rgb(248, 102, 182);
  }
  100% {
    background-color: rgb(216, 39, 136);
  }
}
</style>
