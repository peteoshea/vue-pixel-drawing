<template>
  <div class="colour-picker">
    <Pixel isInColourPicker colour="white" :current="colour == 'white' ? true : false" />
    <Pixel isInColourPicker colour="lightblue" :current="colour == 'lightblue' ? true : false" />
    <Pixel isInColourPicker colour="blue" :current="colour == 'blue' ? true : false" />
    <Pixel isInColourPicker colour="darkblue" :current="colour == 'darkblue' ? true : false" />
  </div>
</template>

<script>
import Pixel from "./Pixel";

export default {
  name: "ColourPicker",
  props: {
    colour: String
  },
  components: {
    Pixel
  }
};
</script>

<style scoped>
.colour-picker {
  margin-right: 20px;
}
</style>
