<template>
  <AppHeader />
  <div>{{ message }}</div>
  <button @click="showAlert">클릭</button>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

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
  components: {
    AppHeader,
  },
};
</script>

<style scoped></style>
