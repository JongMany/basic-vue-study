<template>
  <form action="">
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
export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
};
</script>

<style scoped></style>
