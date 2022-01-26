<template>
  <div class="main-tab-bar">
    <tab-bar>
      <tab-bar-item path="/home" acticeColor="deeppink">
        <img src="~assets/img/tabbar/home.svg" alt="未激活状态下的图标" slot="item-icon">
        <img src="~assets/img/tabbar/home_active.svg" alt="已激活状态下的图标" slot="item-icon-active">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" acticeColor="deeppink">
        <img src="~assets/img/tabbar/category.svg" alt="未激活状态下的图标" slot="item-icon">
        <img src="~assets/img/tabbar/category_active.svg" alt="未激活状态下的图标" slot="item-icon-active">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" acticeColor="deeppink">
        <img src="~assets/img/tabbar/shopcart.svg" alt="未激活状态下的图标" slot="item-icon">
        <img src="~assets/img/tabbar/shopcart_active.svg" alt="未激活状态下的图标" slot="item-icon-active">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" acticeColor="deeppink">
        <img src="~assets/img/tabbar/profile.svg" alt="未激活状态下的图标" slot="item-icon">
        <img src="~assets/img/tabbar/profile_active.svg" alt="未激活状态下的图标" slot="item-icon-active">
        <div slot="item-text">个人中心</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar.vue'
import TabBarItem from 'components/common/tabbar/TabBarItem.vue'
export default {
  name: 'MainTabBar',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style lang="less" scoped>

</style>