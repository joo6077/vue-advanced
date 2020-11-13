<template>
  <div>
      <div v-for="item in fetchedAsk">{{ item.title }}</div>
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