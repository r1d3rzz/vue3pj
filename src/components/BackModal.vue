<template>
  <div class="backdrop" @click.self="closeModal">
    <div
      class="modal"
      :class="{ success: theme === 'success', delete: theme === 'danger' }"
    >
      <slot> Default </slot>
      <slot name="links" />
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "content", "theme"],
  methods: {
    closeModal() {
      this.$emit("closeModal");
    },
  },
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