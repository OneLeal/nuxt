<template>
    <div class="shop">
      <p>商城</p>
      <p class="guss">猜你喜欢情趣内衣</p>
      <div class="shop-container">请 您 挑 选</div>
      <nuxt-link to="/shop/clothes">衣物</nuxt-link>
      <nuxt-link to="/shop/tools">工具</nuxt-link>
      <nuxt-link to="/shop/books">杂志</nuxt-link>
      <nuxt-link to="/shop">猜您喜欢/精品推荐</nuxt-link>
      <nuxt-child />
      <nuxt-link to="/">返回首页</nuxt-link>
    </div>
</template>

<script>
    export default {
        name: "shop"
    }
</script>

<style scoped>
  .shop-container {
    text-align: center;
    height: 35px;
    line-height: 35px;
    background-color: orange;
    color: #fff;
    font-size: 16px;
  }

  .guss {
    width: 200px;
    height: 35px;
    line-height: 35px;
    text-align: center;
    background-color: #f7f7f7;
    padding: 20px;
    border: 1px #ccc solid;
  }
</style>
