<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #24344b;
  /*margin-top: 60px;*/
}
*{
  margin: 0 auto;
  padding: 0;
  list-style:none;
}
body{
  width: 100%;
  height: 100vh;
}
html{
  background: #24344b;
}
</style>

