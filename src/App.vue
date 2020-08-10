<template>
  <div id="app">
    <ColourPicker :colour="colour" />
    <Canvas />
  </div>
</template>

<script>
import Canvas from './components/Canvas.vue';
import ColourPicker from './components/ColourPicker';

export default {
  name: 'App',
  data: function() {
    return {
      colour: 'white',
    };
  },
  components: {
    Canvas,
    ColourPicker,
  },
  mounted() {
    this.$root.$on('updatecolour', (colour) => {
      this.colour = colour;
    });
  },
};
</script>

<style>
#app {
  background-color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 98vh;
}
</style>
