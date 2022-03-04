<template>
  <div class="backdrop">
    <div
      class="modal"
      :class="{ success: theme === 'success', delete: theme === 'danger' }"
    >
      <h1>{{ header }}</h1>
      <p>{{ content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "content", "theme"],
};
</script>

<style scoped>
.backdrop {
  position: fixed;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

.modal {
  width: 400px;
  margin: 100px auto;
  background: white;
  height: 100px;
  padding: 20px;
  border-radius: 5px;
}
p {
  font-style: normal;
}
.success {
  background-color: green;
  color: white;
}
.delete {
  background-color: red;
  color: white;
}
</style>