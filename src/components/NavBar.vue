<template>
    <nav class="menu">
      <ul>
        <li><router-link class="link" :class="{ active: $route.name === 'home' }" to="/">Home</router-link></li>
        <li><router-link class="link" :class="{ active: $route.name === 'about' }" to="/about">About</router-link></li>
        <li><router-link class="link" :class="{ active: $route.name === 'accessories' }" to="/accessories">Accessories</router-link></li>
        <li><router-link class="link" :class="{ active: $route.name === 'souvenirs' }" to="/souvenirs">Souvenirs</router-link></li>
        <li><router-link class="link" :class="{ active: $route.name === 'vue-app' }" to="/vue-app">Vue App</router-link></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NavBar'
  }
  </script>
  
  <style scoped>
  </style>