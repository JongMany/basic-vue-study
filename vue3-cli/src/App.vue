<template>
  <div>{{ message }}</div>
  <button @click="showAlert">클릭</button>
</template>

<script>
export default {
  data() {
    return {
      message: 'hi',
    };
  },
  methods: {
    showAlert() {
      alert('HelloWorld');
    },
  },
};
</script>

<style scoped></style>
