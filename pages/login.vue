<template>
    <div class="login">
      <p>请登录</p>
      <el-button type="primary" @click="login">登 陆</el-button>
    </div>
</template>

<script>
    export default {
        name: "login",
        layout: 'ampty',
        methods: {
          login() {
            this.$router.push('/')
          }
        },
    }
</script>

<style scoped>
  .login {
    width: 300px;
    height: 300px;
    background-color: #f5f5f5;
    border: 1px #d8d8d8 solid;
  }
</style>
