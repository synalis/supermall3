<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="blue">
      <template #item-icon>
        <router-link to="/home"><img src="../assets/img/tabbar/home.svg" alt=""></router-link>
      </template>
      <template #item-active>
        <router-link to="/home"><img src="../assets/img/tabbar/home_active.svg" alt=""></router-link>
      </template>
      <template #item-text>
        <router-link to="/home"><p>首页</p></router-link>
      </template>
    </tab-bar-item>
    <tab-bar-item  path="/about" activeColor="pink">
      <template #item-icon>
        <router-link to="/about"> <img src="../assets/img/tabbar/category.svg" alt=""></router-link>
      </template>
      <template #item-active>
        <router-link to="/about"><img src="../assets/img/tabbar/category_active.svg" alt=""></router-link>
      </template>
      <template #item-text>
        <router-link to="/about"><p>关于</p></router-link>
      </template>
    </tab-bar-item>
    <tab-bar-item path="/shopCart">
      <template #item-icon>
        <router-link to="/shopCart"><img src="../assets/img/tabbar/shopcart.svg" alt=""></router-link>

      </template>
      <template #item-active>
        <router-link to="/shopCart"><img src="../assets/img/tabbar/shopcart_active.svg" alt=""></router-link>
      </template>
      <template #item-text>
        <router-link to="/shopCart"><p>购物车</p></router-link>
      </template>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <template #item-icon>
        <router-link to="/profile"><img src="../assets/img/tabbar/profile.svg" alt=""></router-link>
      </template>
      <template #item-active>
        <router-link to="/profile"><img src="../assets/img/tabbar/profile_active.svg" alt=""></router-link>
      </template>
      <template #item-text>
        <router-link to="/profile"><p>我的</p></router-link>
      </template>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from "./tabbar/TabBar";
import TabBarItem from "./tabbar/TabBarItem";
export default {
  name: "MainTabBar",
  components:{
    TabBar,
    TabBarItem
  }
}

</script>

<style scoped>

</style>