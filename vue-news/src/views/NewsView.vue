<template>
  <div>
      <p v-for="(item, index) in this.$store.state.news" :key="index">
        <a :href="item.url">
          {{ item.title }}
        </a>
      </p>
  </div>
</template>

<script>
import { fetchNewsList } from '../api/index.js'

export default {
  created() {
    this.$store.dispatch('FETCH_NEWS');

    // var vm = this;
    // fetchNewsList()
    // .then(function(response) {
    //   console.log(response);
    //   vm.users = response.data;
    // })
    // .catch(function(error) {
    //   console.log(error);
    // })
  },
}
</script>

<style>

</style>