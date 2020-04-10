<template>
  <div id="app">
    <div id="nav">
      <Header />
    </div>
    <router-view/>
  </div>
</template>
<script>
import Header from './components/Header';
export default {
  name: 'app',
  components: {
    Header
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
}
#nav {
  margin-bottom: 6.4rem;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
body {
  background: linear-gradient(45deg, rgb(37, 211, 211), rgb(30, 212, 112))
}
</style>
