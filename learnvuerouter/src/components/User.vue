<template>
  <div>
    <h2>我是用户界面</h2>
    <p>用户界面，嘿嘿嘿</p>
    <p>用户id：{{userId}}</p>
  </div>
</template>

<script>
export default {
  name: "User",
  computed: {
    userId() {
      return this.$route.params.userId
    }
  }
}
</script>

<style scoped>

</style>
