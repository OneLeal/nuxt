<template>
  <div class="layout-default">
    <Header />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
  import Header from '../components/header'
  import Footer from  '../components/footer'
  export default {
    components: { Header, Footer }
  }
</script>

<style scoped>
  *{
    margin: 0;
    padding: 0;
  }

  .layout-default {

  }
</style>
