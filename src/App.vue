<template>
  <h1>Hello World</h1>
  <BackModal />
</template>

<script>
import BackModal from "./components/BackModal.vue";
export default {
  components: {
    BackModal,
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>