<template>
    <div class="my-check-box">
      <div class="icon-style" v-show="!status">
        <i :class="['iconfont']">&#xe631;</i>
      </div>
      <div class="icon-style" v-show="status">
        <i :class="['iconfont', { 'active': status }]">&#xe634;</i>
      </div>

      <div>
        <input
          class="check-icon"
          type="checkbox"
          :checked="checked"
          @change="handleChange"
        />
      </div>
      <div>
        <slot />
      </div>
    </div>
</template>

<script>
    export default {
        name: "my-check-box",
        props: {
          checked: { type: Boolean, default: false }
        },
        data() {
          return {
            status: this.checked,
          }
        },
        methods: {
          handleChange() {
            this.status = event.target.checked
            this.$emit('change', event.target.checked)
          }
        },
    }
</script>

<style scoped lang="scss">
  .my-check-box {
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;

    .check-icon {
      cursor: pointer;
      opacity: 0;
    }

    .icon-style {
      position: absolute;
      top: 0;
      left: 0;

      .active {
        color: #007aff;
      }
    }

    .iconfont {
      font-size: 14px;
      color: #ccc;
      transition: all .5s;

      &:hover {
        color: blue;
      }
    }
  }
</style>
