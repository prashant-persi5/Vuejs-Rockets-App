<template>
  <section class="row">
    <rocket v-for="rocket in rockets"
    :key="rocket.name"
    :rocket="rocket"
    :removeRocket="removeRocket"></rocket>
  </section>
</template>

<script>
import Rocket from '@/components/Rocket';

export default {
  name: 'rocket-list',
  components: {
    Rocket,
  },
  props: ['rockets', 'removeRocket'],
};
</script>
