<template>
  <div id="app">
    <!-- Навигация будет в каждом компоненте, поэтому здесь только router-view -->
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
/* Глобальные стили */
@import './assets/css/style.css';

/* Основные стили приложения */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>