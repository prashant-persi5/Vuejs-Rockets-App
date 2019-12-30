<template>
  <section>
    <new-rocket-form></new-rocket-form>
    {{rockets}}
  </section>
</template>

<script>
import NewRocketForm from '@/components/NewRocketForm';
import API from '@/lib/API';

export default {
  name: 'rockets',
  components: {
    NewRocketForm
  },
  data: () => ({
    rockets: [],
  }),
  async mounted() {
    this.rockets = await API.getRockets();
  },
};
</script>

<style>

</style>