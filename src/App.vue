<template>
  <div id="app" class="bg-black h-screen">
    <head>
      <meta charset="UTF-8">
      <title>TODO-1</title>
    </head>
    <MainPage/>
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue'

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style>
#app {
  font-family: Roboto, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
