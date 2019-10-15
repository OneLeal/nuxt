<template>
    <div class="vertical">
      <Articles />
      <Nuxt />
    </div>
</template>

<script>
  import Articles from '../components/articles'
    export default {
        name: "vertical",
        components: { Articles },
    }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }

  .vertical {
    display: flex;
    justify-content: flex-start;
  }
</style>
