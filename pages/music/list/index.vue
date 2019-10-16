<template>
    <div>
      <VueSlideUpDown :active="flag" :duration="1000">
        <ul>
          <li v-for="(item, index) of musicList" :key="item">
            <span>{{ index }}.</span>
            <span>{{ item }}</span>
          </li>
        </ul>
      </VueSlideUpDown>

      <el-button type="primary" @click="flag = !flag">{{ flag ? '收 起' : '展 开' }}</el-button>
    </div>
</template>

<script>
  import VueSlideUpDown from 'vue-slide-up-down'
  import Vue from 'vue'
  Vue.component('vue-slide-up-down', VueSlideUpDown)
  export default {
        name: "index",
        components: { VueSlideUpDown },
        data() {
          return {
            flag: true,
            musicList: [
              '庸人自扰', '只是太爱你', '雅俗共赏', '童话镇', '起风了', '那女孩对我说', '最近'
            ]
          }
        }
    }
</script>

<style scoped>

</style>
