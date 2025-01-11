<template>
  <AppHeader v-bind:appTitle="message" v-on:change="changeTitle" />
  <div>{{ message }}</div>
  <button @click="showAlert">클릭</button>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data() {
    return {
      message: '앱 헤더 컴포넌트',
    };
  },
  methods: {
    showAlert() {
      alert('HelloWorld');
    },
    changeTitle(props1, props2) {
      console.log(props1, props2);
      this.message = `${props1} ${props2}`;
    },
  },
  components: {
    AppHeader,
  },
};
</script>

<style scoped></style>
