<template>
  <h1>Hello {{ title }}</h1>
</template>

<script>
export default {
  data() {
    return {
      title: "Rider",
    };
  },
};
</script>

<style>
h1 {
  color: blue;
}
</style>