<template>
  <div
    class="container-fluid vh-100 d-flex justify-content-center align-items-center"
  >
    <DadJokes />
  </div>
</template>

<script>
import DadJokes from './components/DadJokes.vue';

export default {
  name: 'App',
  components: { DadJokes },
};
</script>

<style lang="scss">
.container-fluid {
  background: #ffb6c1;
}
</style>
