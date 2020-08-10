<template>
  <div class="colour-picker">
    <Pixel interactive colour="white" :current="colour == 'white' ? true : false" />
    <Pixel interactive colour="lightblue" :current="colour == 'lightblue' ? true : false" />
    <Pixel interactive colour="blue" :current="colour == 'blue' ? true : false" />
    <Pixel interactive colour="darkblue" :current="colour == 'darkblue' ? true : false" />
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
