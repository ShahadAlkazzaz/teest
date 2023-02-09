<script setup></script>

<template>
  <div id="container">
    <img
      id="Hero-img"
      src="../assets/img/happy-cute-baby-lying-on-white-sheet-1070045180_1257x838.jpeg"
      alt="Baby"
      class="img-fluid"
    />
    <div class="upp">
      <p>50-70% OFF</p>
    </div>
    <div class="down">
      <p>Winter sale</p>
    </div>
  </div>
</template>

<style scoped>
#Hero-img {
  /* opacity: 0.7; */
  filter: blur(2px);
  width: 100%;
}
#container {
  overflow-x: hidden;
  margin: 0 auto;
  height: auto;
}
.upp {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: black;
  font-size: 30px;
  font-weight: 500;
  animation-name: example;
  animation-duration: 10s;
  animation-iteration-count: 30;
}

.down {
  position: absolute;
  top: 70%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 50px;
  font-weight: 500;
  color: black;
}

@keyframes example {
  0% {
    background-color: red;
  }
  25% {
    background-color: rgb(63, 200, 191);
  }
  50% {
    background-color: blue;
  }
  100% {
    background-color: rgb(216, 39, 136);
  }
}
</style>
