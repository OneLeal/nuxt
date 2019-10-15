<template>
    <div>
      <p>歌单详情</p>
      <nuxt-link to="/music/list/info">歌单推荐 →</nuxt-link>
      <nuxt-link to="/music/list/me">我的歌单 →</nuxt-link>
      <nuxt-link to="/music/list/recently">最近播放 →</nuxt-link>
      <Nuxt />
      <nuxt-link to="/music">返回音乐馆</nuxt-link>
    </div>
</template>

<script>
    export default {
        name: "list"
    }
</script>

<style scoped>

</style>
