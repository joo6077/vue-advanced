<template>
  <div>
      <p v-for="(item, index) in fetchedAsk" :key="index">
        <router-link :to="`item/${item.id}`">
          {{ item.title }}
        </router-link>
        <small>{{ item.time_ago }} by {{ item.user }}</small>
      </p>
  </div>
</template>

<script>
import { mapGetters, mapState } from 'vuex'

export default {
  computed: {
    // ...mapState({
    //   ask: state => state.ask
    // }),
    ...mapGetters([
      'fetchedAsk'
    ])
  },
  // 속성 함수
  created() {
    this.$store.dispatch('FETCH_ASK');
  },
}
</script>

<style>

</style>