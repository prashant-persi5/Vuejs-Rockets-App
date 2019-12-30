<template>
  <section>
    <new-rocket-form></new-rocket-form>
    <rocket-list :rockets="rockets"></rocket-list>
  </section>
</template>

<script>
import NewRocketForm from '@/components/NewRocketForm';
import RocketList from '@/components/RocketList';
import API from '@/lib/API';

export default {
  name: 'rockets',
  components: {
    NewRocketForm,
    RocketList,
  },
  data: () => ({
    rockets: [],
  }),
  async mounted() {
    this.rockets = await API.getRockets();
    console.log(this.rockets);
  },
};
</script>

<style>

</style>