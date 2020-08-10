<template>
  <div>
    <Pixel colour="white" :current="colour == 'white' ? true : false" />
    <Pixel colour="lightblue" :current="colour == 'lightblue' ? true : false" />
    <Pixel colour="blue" :current="colour == 'blue' ? true : false" />
    <Pixel colour="darkblue" :current="colour == 'darkblue' ? true : false" />
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
