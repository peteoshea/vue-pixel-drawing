<template>
  <div class="canvas">
    <Pixel isInCanvas v-for="(colour, index) in pixels" :key=index :colour=colour :index=index />
  </div>
</template>

<script>
import Pixel from "./Pixel";

export default {
  name: "Canvas",
  components: {
    Pixel
  },
  props: {
    pixels: Array
  }
};
</script>

<style scoped>
.canvas {
  display: flex;
  flex-wrap: wrap;
  max-width: 900px;
}
</style>
