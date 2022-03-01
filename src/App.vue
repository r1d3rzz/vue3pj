<template>
  <h1 ref="title">Hello {{ title }}</h1>
  <input type="text" name="" ref="name" id="" />
  <button @click="clickHandler">click</button>
</template>

<script>
export default {
  data() {
    return {
      title: "Rider",
    };
  },
  methods: {
    clickHandler() {
      this.$refs.name.focus();
      this.$refs.title.textContent = "Welcome";
    },
  },
};
</script>

<style>
h1 {
  color: blue;
}
</style>