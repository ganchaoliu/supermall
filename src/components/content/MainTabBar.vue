<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="#df7575">
      <img src="../assets/img/1.png" alt="" slot="item-icon"/>
      <img src="../assets/img/11.png" alt="" slot="item-icon-active"/>
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="#df7575">
      <img src="../assets/img/2.png" alt="" slot="item-icon"/>
      <img src="../assets/img/22.png" alt="" slot="item-icon-active"/>
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="#df7575">
      <img src="../assets/img/3.png" alt="" slot="item-icon"/>
      <img src="../assets/img/33.png" alt="" slot="item-icon-active"/>
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="#df7575">
      <img src="../assets/img/4.png" alt="" slot="item-icon"/>
      <img src="../assets/img/44.png" alt="" slot="item-icon-active"/>
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  const TabBar =()=>import('./tabbar/TabBar')
  const TabBarItem =()=>import('./tabbar/TabBarItem')

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
