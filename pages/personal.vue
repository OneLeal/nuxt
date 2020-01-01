<template>
    <div class="personal">
      <p>个人中心</p>

      <div v-for="item of arr" :key="item.name">
        <CheckBox
          :checked="item.checked"
          class="check-box-item"
          @change="checkedChange">
          <div>{{ item.name }}</div>
        </CheckBox>
      </div>
      <nuxt-link to="/">返回首页</nuxt-link>
    </div>
</template>

<script>
  import CheckBox from '../components/my-check-box'
    export default {
        name: "personal",
        components: { CheckBox },
        layout: 'vertical',
        data() {
          return {
            arr:[
              { name: '邓紫棋', checked: true },
              { name: '周杰伦', checked: true },
              { name: '周传雄', checked: false },
              { name: '陈雪凝', checked: false },
              { name: '赵方婧', checked: false },
            ]
          }
        },
        methods: {
          checkedChange(value) {
            console.log(value)
          }
        }
    }
</script>

<style scoped>
  .check-box-item {
    margin: 5px 20px;
  }
</style>
