<template>
  <div id="app">
    <ColourPicker :colour="colour" />
    <Canvas />
  </div>
</template>

<script>
import Canvas from "./components/Canvas.vue";
import ColourPicker from "./components/ColourPicker";

export default {
  name: "App",
  data: function() {
    return {
      colour: "white"
    };
  },
  components: {
    Canvas,
    ColourPicker
  },
  mounted() {
    this.$root.$on("updatecolour", colour => {
      this.colour = colour;
    });
  }
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
