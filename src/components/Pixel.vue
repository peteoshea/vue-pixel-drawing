<template>
  <div
    @click="interactive && changeColour(colour)"
    :class="['pixel', colour, current ? 'current' : '']"
  ></div>
</template>

<style scoped>
.pixel {
  border: 1px solid lightgray;
  width: 30px;
  height: 30px;
  box-sizing: border-box;
}
.pixel.current {
  border: 4px solid yellow;
}
.white {
  background-color: white;
}
.lightblue {
  background-color: rgb(0, 188, 212);
}
.blue {
  background-color: rgb(3, 169, 244);
}
.darkblue {
  background-color: rgb(33, 150, 243);
}
</style>

<script>
export default {
  name: 'Pixel',
  props: {
    colour: String,
    current: Boolean,
    interactive: Boolean,
  },
  methods: {
    changeColour: function(colour) {
      this.$root.$emit('updatecolour', colour);
    },
  },
};
</script>
