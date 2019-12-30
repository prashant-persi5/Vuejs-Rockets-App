<template>
  <section>
    <button @click="showForm = !showForm" type="button" class="btn btn-danger">Show Form</button>
    <form v-if="showForm">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" class="form-control" name="name" id="name" value="">
      </div>
      <div class="form-group">
        <label for="country">Country</label>
        <input type="text" class="form-control" name="country" id="country" value="">
      </div>
      <div class="form-group">
        <label for="description">Description</label>
        <textarea class="form-control" name="description" id="description"></textarea>
      </div>
      <div class="form-group">
        <label for="image">Image</label>
        <input type="text" class="form-control" name="image" id="image" value="">
      </div>
      <button type="button" class="btn btn-success">Add Rocket</button>
    </form>
  </section>
</template>

<script>
export default {
  data: () => ({
    showForm: false,
  }),
};
</script>

<style>

</style>