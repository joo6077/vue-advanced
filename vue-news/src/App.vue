<template>
  <div id="app">
    <!-- strongly recommended -->
    <!-- <ToolBar></ToolBar> -->
    <!-- essential -->
    <tool-bar></tool-bar>
    <!-- 여기 안에 구현 라우터가 구현됨. -->
    <transition name="page">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
/* eslint-disable */
import ToolBar from './components/ToolBar.vue'
export default {
  components: {
    ToolBar,
  }
}
</script>

<style>
body{
  padding: 0;
  margin: 0;
}

/* Router Transition */
.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-to /* .page-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
