<template>
  <div id="app" class="d-flex flex-column">
    <navbar />
    <router-view class="flex-grow-1" />
    <footer-row />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import FooterRow from "./components/FooterRow.vue"
export default {
  components: {
    Navbar,
    FooterRow
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
  min-height: 100vh;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
