<template>
  <h1>Hello World</h1>
  <div v-if="showModal">
    <BackModal :theme="theme" @closeModal="showModal = false">
      <h1>Welcome</h1>
      <p>welcome user myint thway khine</p>
      <template v-slot:links>
        <a href="">Nothing</a>
      </template>
    </BackModal>
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
</style>