<script></script>

<template>
  <div id="photos" class="col">
    <div class="card" style="width: 18rem">
      <div class="card-body">
        <h5 class="card-title">{{ sale.name }}</h5>
        <p class="card-text">
          {{ sale.price }}
        </p>
        <a href="#" class="btn btn-primary">BUY</a>
      </div>
      <img :src="sale.image"  class="card-img-bottom" alt="..." />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    sale: {
      required: true,
      type: Object,
    },
  },
};
</script>

<style scoped>
#photos{
    margin-bottom: 50px;
}
</style>
