<template>
  <div id="app">
    <Card />
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'app',
  components: {
    Card
  }
}
</script>

<style>

html, body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

#app {
  color: #2c3e50;
}
</style>
