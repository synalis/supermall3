<template>
  <div class="tab-bar-item" @click="itemClick">
    <div>
      <div v-if="!isActive">
        <slot name="item-icon"></slot>
      </div>
      <div v-else>
        <slot name="item-active"></slot>
      </div>
      <div :style="activeStyle">
        <slot name="item-text"></slot>
      </div>

    </div>
    <!--    <router-link to="/"><img src="../../assets/img/tabbar/home.svg" alt=""></router-link>-->
    <!--    <router-link to="/about" ><img src="../../assets/img/tabbar/category.svg" alt=""><p>关于</p></router-link>-->
    <!--    <div class="tab-bar-item">首页</div>-->
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props:{
    path:String,
    activeColor:{
      type:String,
      default:'red'
    }
  },
  data() {
    return {
      // isActive: true
    }
  },
  computed:{
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle(){
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods:{
    itemClick (){
      // console.log('点击了')
      this.$router.replace(this.path)
    }
  }
}

</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
  /*line-height: 49px;*/
}

.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
}

.router-link-active{
  text-decoration: none;
  color: red;
}
a {
  text-decoration: none;
}
</style>