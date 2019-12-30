<template>
  <section>
    <nav-bar></nav-bar>
    <rockets class="container mt-2"></rockets>
  </section>
</template>

<script>
import NavBar from '@/components/NavBar';
import Rockets from '@/views/Rockets';

export default {
  name: 'app',
  components: {
    NavBar,
    Rockets,    
  },
};
</script>
