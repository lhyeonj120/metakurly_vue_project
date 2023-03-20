<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <router-link class="navbar-brand" :to="{name: 'Home'}">Home</router-link>
    <ul class="navbar-nav mr-auto">
      <li class="nav-iem active">
        <router-link class="nav-link" :to="{name: 'Best'}">Best</router-link>
      </li>
      <li class="nav-iem active">
        <router-link class="nav-link" :to="{name: 'Product'}">Product</router-link>
      </li>
      <li class="nav-iem active">
        <router-link class="nav-link" :to="{name: 'myPage'}">myPage</router-link>
      </li>
    </ul>
  </nav>
  <div class="container">
    <router-view/>
  </div>
</template>

<script>
export default {
  
}
</script>

<style>

</style>
