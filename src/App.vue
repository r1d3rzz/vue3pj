<template>
  <h1>Hello Vue</h1>
  <div v-if="showModal">
    <BackModal :theme="theme" @closeModal="showModal = false">
      <h1>Welcome</h1>
      <p>welcome user myint thway khine</p>
      <template v-slot:links>
        <a href="">Nothing</a>
      </template>
    </BackModal>
  </div>

  <div v-if="showModal_2">
    <BackModal theme="danger" @closeModal="showModal_2 = false">
      <h1>Delete Modal</h1>
      <p>Delete user myint thway khine</p>
      <template v-slot:links>
        <a href="">Nothing</a>
      </template>
    </BackModal>
  </div>

  <button @click="showModal = true">open modal</button>
  <br /><br /><br />
  <button @click="showModal_2 = true">delete modal</button>
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
      showModal_2: false,
    };
  },
};
</script>

<style scoped>
</style>