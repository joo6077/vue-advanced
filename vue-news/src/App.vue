<template>
  <div id="app">
    <!-- strongly recommended -->
    <!-- <ToolBar></ToolBar> -->
    <!-- essential -->
    <tool-bar></tool-bar>
    <!-- 여기 안에 구현 라우터가 구현됨. -->
    <router-view></router-view>
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
</style>
