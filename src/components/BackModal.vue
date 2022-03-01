<template>
  <div class="backdrop">
    <div class="modal"><p>Modal Content</p></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
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
  padding: 10px;
  border-radius: 5px;
  text-align: center;
}
</style>