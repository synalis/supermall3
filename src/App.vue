<template>
  <div id="nav">
   <main-tab-bar></main-tab-bar>
  </div>
  <router-view/>
</template>

<script>
import MainTabBar from "./components/MainTabBar";

export default {
  name: 'nav',
  components: {
    MainTabBar
  }
}
</script>


<style>
/*在style里面引用资源要用@*/
@import "assets/css/base.css";



</style>

