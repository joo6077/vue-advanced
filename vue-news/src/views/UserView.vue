<template>
  <div>
      <p>id : {{ userInfo.id }}</p>
      <p>karma : {{ userInfo.karma }}</p>
      <p>created : {{ userInfo.created }}</p>
  </div>
</template>

<script>
export default {
    computed: {
     userInfo() {
        return this.$store.state.user;
     }   
    },
    created() {
        const userName = this.$route.params.id;
        // 객체 하나만 넘겨야함.
        this.$store.dispatch('FETCH_USER', userName);
        // axios.get(`https://api.hnpwa.com/v0/user/${userName}.json`)
    },
}
</script>

<style>

</style>