<template>
  <nav class="navbar navbar-dark navbar-expand bg-dark text-light">
    <div class="navbar-brand">
      <img src="../assets/logo.png" width="45" height="45" alt loading="lazy" />
      <span class="ml-2">Vue Gregslist</span>
    </div>
    <ul class="navbar-nav mr-auto">
      <li
        class="nav-item"
        :class="{ active: $route.name == 'Cars' || $route.name == 'CarDetails' }"
      >
        <router-link :to="{ name: 'Cars' }" class="nav-link">Cars</router-link>
      </li>
      <li class="nav-item" :class="{ active: $route.name == 'Jobs' }">
        <router-link :to="{ name: 'Jobs' }" class="nav-link">Jobs</router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<style>
</style>