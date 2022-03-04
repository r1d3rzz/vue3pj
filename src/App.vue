<template>
  <h1>Hello World</h1>
  <div v-if="showModal">
    <BackModal
      :header="header"
      content="Welcome Users"
      :theme="theme"
      @closeModal="showModal = false"
    />
  </div>
  <button @click="showModal = true">open modal</button>
</template>

<script>
import BackModal from "./components/BackModal.vue";
export default {
  components: {
    BackModal,
  },
  data() {
    return {
      header: "Login Successful",
      theme: "success",
      showModal: false,
    };
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>