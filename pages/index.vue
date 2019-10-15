<template>
  <div class="container">
    <div>
      <nuxt-link to="/music">音 乐 馆</nuxt-link>
      <nuxt-link to="/shop">商 城</nuxt-link>
      <nuxt-link to="/personal">个人中心</nuxt-link>
    </div>
    <el-button type="text" @click="loginOut">退 出</el-button>
  </div>
</template>

<script>

export default {
  methods: {
    loginOut() {
      this.$router.push('/login')
    }
  }
}
</script>

<style scoped>
  .container {

  }
</style>
