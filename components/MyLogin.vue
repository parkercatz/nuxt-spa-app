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
  computed: {
    isLogin() {
      return this.$store.state.isLogin
    },
  },
  methods: {
    login: function() {
      this.$store.commit('login')
    },
    logout: function() {
      this.$store.commit('logout')
    },
  },
}
</script>
