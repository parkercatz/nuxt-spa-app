<template>
  <section>
    <h1>ログイン状態</h1>
    <p>{{ isLogin }}</p>
    <button v-on:click="login()">ログイン</button>
    <button v-on:click="logout()">ログアウト</button>
  </section>
</template>

<script>
export default {
  data() {
    return { isLogin: true }
  },
  methods: {
    login: function() {
      this.isLogin = true
    },
    logout: function() {
      this.isLogin = false
    },
  },
}
</script>
