<template>
  <div>
    <list-item></list-item>
    <!-- <ul class="news-list">
      <li class="post" v-for="(item, index) in fetchedAsk" :key="index">
        <div class="points">
          {{ item.points }}
        </div>
        <div>
          <p class="news-title">
            <router-link :to="`item/${item.id}`">
              {{ item.title }}
            </router-link>
          </p>
          <small class="link-text">
            {{ item.time_ago }} by 
            <router-link class="link-text" :to="'/user' + item.user">{{ item.user }}</router-link>
          </small>
        </div>
      </li>
    </ul> -->
  </div>
</template>

<script>
// import { mapGetters, mapState } from 'vuex'
import ListItem from '../components/ListItem.vue'


export default {
  components: {
    ListItem,
  },
  // computed: {
    // ...mapState({
    //   ask: state => state.ask
    // }),
    // ...mapGetters([
      // 'fetchedAsk'
    // ])
  // },
  // 속성 함수
  created() {
    this.$store.dispatch('FETCH_ASK');
  },
}
</script>

<style scoped>

</style>