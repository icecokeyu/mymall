<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
  props: {
    path: {
      type: String,
      default: ''
    },
    activeColor: {
      type: String,
      default: 'pink'
    }
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    // 点击item跳转到对应的路由地址
    itemClick() {
      this.$router.push(this.path)
    }
  }
}
</script>

<style lang="less" scoped>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
    img {
      height: 24px;
      width: 24px;
      margin-top: 4px;
      margin-bottom: 2px;
      vertical-align: middle;
    }
  }
</style>