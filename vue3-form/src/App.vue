<template>
  <form action="" @submit.prevent="submitForm">
    <div>
      <label for="id">아이디</label>
      <input type="text" id="id" v-model="username" />
    </div>
    <div>
      <label for="password">비밀번호</label>
      <input type="password" id="password" v-model="password" />
    </div>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
import axios from 'axios';
import { ref } from 'vue';
export default {
  //   data() {
  //     return {
  //       username: '',
  //       password: '',
  //     };
  //   },
  //   methods: {
  //     async submitForm() {
  //       // event.preventDefault();
  //       try {
  //         const response = await axios.post(
  //           'https://jsonplaceholder.typicode.com/users',
  //           {
  //             username: this.username,
  //             password: this.password,
  //           },
  //         );

  //         if (response.status === 201) {
  //           alert('로그인 성공');
  //         }
  //       } catch (error) {
  //         console.error(error);
  //       }
  //     },
  //   },
  setup() {
    // data
    const username = ref('');
    const password = ref('');

    //methods
    const submitForm = async () => {
      try {
        const response = await axios.post(
          'https://jsonplaceholder.typicode.com/users',
          {
            username: username.value,
            password: password.value,
          },
        );

        if (response.status === 201) {
          alert('로그인 성공');
        }
      } catch (error) {
        console.error(error);
      }
    };

    return {
      username,
      password,
      submitForm,
    };
  },
};
</script>

<style scoped></style>
