<template>
    <div class="tab-bar-item" @click="tabBarItemClick">
      <div v-if="!isActive">
        <slot name="item-icon" ></slot>
      </div>
      <div v-else>
        <slot name="item-icon-active" ></slot>
      </div>
      <div :style="activeStyle">
        <slot name="item-text"></slot>
      </div>
<!--      <img src="../../assets/img/1.png" alt="" />-->
<!--      <div>首页</div>-->
    </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    data(){
      return{
        // isActive: true
      }
    },
    props:{
      path:String,
      activeColor:{
        type:String,
        default:'#df7575'
      }
    },
    methods:{
      tabBarItemClick(){
        this.$router.push(this.path)
      }
    },
    computed:{
      isActive(){
        return this.$route.path.indexOf(this.path)!=-1
      },
      activeStyle(){
        return this.isActive ? {color:this.activeColor} :{}
      }
    },

  }
</script>

<style scoped>
  .tab-bar-item{
    height: 49px;
    text-align: center;
    flex: 1;
    /*line-height: 49px;*/
    font-size: 12px;
    color: #333;
  }
  .tab-bar-item img{
    height: 24px;
    width: 24px;
    margin-top: 4px;
    margin-bottom: 2px;
    vertical-align: middle;
   }

</style>
