<template>
  <div>
      <section>
          <!-- 질문 상세 정보 -->
          <div>
              <div>
                  User
              </div>
              <div>
                  사용자 정보
              </div>
              <h2>{{ fetchedItem.title }}</h2>
          </div>
      </section>
      <section>
          <!-- 질문 댓글 -->
      </section>
      <!-- <p>{{fetchedItem.title}}</p>
      <div>
          {{ fetchedItem.content }}
      </div> -->
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
    computed: {
        ...mapGetters(['fetchedItem']),
    },
    created() {
        const itemId = this.$route.params.id;
        this.$store.dispatch('FETCH_ITEM', itemId);
    },
}
</script>

<style>

</style>