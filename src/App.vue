<template>
  <h1>Hello World</h1>
  <BackModal :header="header" :content="content" :theme="theme" />
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
      content: "Welcome User",
      theme: "success",
    };
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>