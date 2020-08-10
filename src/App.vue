<template>
  <div id="app">
    <ColourPicker />
    <Canvas />
  </div>
</template>

<script>
import Canvas from './components/Canvas.vue';
import ColourPicker from './components/ColourPicker'

export default {
  name: 'App',
  components: {
    Canvas,
    ColourPicker,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
