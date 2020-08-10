<template>
  <div id="app">
    <ColourPicker :colour="colour" />
    <Canvas :pixels="pixels" />
  </div>
</template>

<script>
import Canvas from "./components/Canvas.vue";
import ColourPicker from "./components/ColourPicker";

const defaultColour = "white";

export default {
  name: "App",
  data: function() {
    return {
      colour: defaultColour,
      pixels: Array(30 * 30)
        .fill()
        .map(() => defaultColour)
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
    this.$root.$on("clickedpixel", index => {
      this.pixels.splice(index, 1, this.colour);
    });
  }
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
