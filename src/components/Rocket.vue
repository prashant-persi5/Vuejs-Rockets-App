<template>
  <div class="card col-4">
    <img :src="rocket.image" class="card-img-top rocket-image" alt="rocket.name">
    <div class="card-body">
      <h5 class="card-title">{{rocket.name}}</h5>
      <p class="card-text">{{rocket.description}}</p>
      <button @click="removeRocket" class="btn btn-danger">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'rocket',
  props: ['rocket', 'removeRocket'],
};
</script>

<style>
.rocket-image {
  max-height: 400px;
  width: auto;
}
</style>