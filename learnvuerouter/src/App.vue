<template>
  <div id="app">
    <router-view></router-view>
    <router-link to="/home">首页</router-link>
    <router-link to="/about">关于</router-link>
<!--    <button @click="homeClick">首页</button>-->
<!--    <button @click="aboutClick">关于</button>-->
    <router-link :to="'/user/' + userId">用户</router-link>
    <router-link :to="{path: '/profile', query:{name: 'why', age: 18, height: 1.88}}">档案</router-link>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    homeClick() {
      this.$router.push('/home')
    },
    aboutClick() {
      this.$router.push('/about')
    }
  },
  data() {
    return {
      userId: 'lisi'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.active{
  color: red
}
</style>
