<template>
  <section>
    <button @click="showForm = !showForm" type="button" class="btn btn-danger">Show Form</button>
    <form v-if="showForm" @submit.prevent="onAddRocket">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" v-model="rocket.name" class="form-control" name="name" id="name" value="">
      </div>
      <div class="form-group">
        <label for="country">Country</label>
        <input type="text" v-model="rocket.country" class="form-control" name="country" id="country" value="">
      </div>
      <div class="form-group">
        <label for="description">Description</label>
        <textarea class="form-control" v-model="rocket.description" name="description" id="description"></textarea>
      </div>
      <div class="form-group">
        <label for="image">Image</label>
        <input type="text" v-model="rocket.image" class="form-control" name="image" id="image" value="">
      </div>
      <button type="submit" class="btn btn-success">Add Rocket</button>
    </form>
  </section>
</template>

<script>
function getEmptyRocket() {
  return {
    name: '',
    description: '',
    country: '',
    image: '',
  };
}

export default {
  props: ['addRocket'],
  data: () => ({
    showForm: false,
    rocket: getEmptyRocket(),
  }),
  methods: {
    onAddRocket() {
      this.addRocket(this.rocket);
      this.rocket = getEmptyRocket();
      this.showForm = false;
    }
  }
};
</script>
