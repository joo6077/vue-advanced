<template>
  <div id="app">
    <!-- strongly recommended -->
    <!-- <ToolBar></ToolBar> -->
    <!-- essential -->
    <tool-bar></tool-bar>
    
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
