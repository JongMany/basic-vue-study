<template>
  <h1>{{ appTitle }}</h1>
  <button @click="changeTitle">변경</button>
</template>

<script>
export default {
  props: ['appTitle'],
  methods: {
    changeTitle() {
      this.$emit('change', '변경!', '변경2!');
    },
  },
};
</script>

<style scoped></style>
