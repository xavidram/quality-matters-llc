<template>
  <div id="app">
    <AppNav />
    <router-view/>
    <footer class="app-footer"></footer>
  </div>
</template>
<script>
import AppNav from './components/AppNav'
export default {
  components: { AppNav }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.app-footer {
  height: 32px;
  background: #484848;
}
</style>
