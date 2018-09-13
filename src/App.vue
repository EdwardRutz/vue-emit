<template>
  <div>
    <div id="app">
      <img alt="Vue logo" src="./assets/logo.png">
      <Welcome msg="Parent/Child Data Flow with Props and Events"/>
      <br><br>
      <input type="text" v-model="adjective" @adjectiveReset="adjective = $event">
    </div>
  </div>
</template>

<script>
import Welcome from './components/Welcome.vue'

export default {
  name: 'app',
  adjective: 'Add Superlatives Here...',
  components: {
    Welcome
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
  image {
    text-align: center;
  }
</style>
