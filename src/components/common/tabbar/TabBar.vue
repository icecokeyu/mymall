<template>
  <div class="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBar'
}
</script>

<style lang="less" scoped>
  .tab-bar {
    display: flex;
    position: fixed;
    width: 100%;
    background-color: #f6f6f6;
    bottom: 0;
    box-shadow: 0 -1px 1px rgba(100, 100, 100, 0.2);
  }
</style>