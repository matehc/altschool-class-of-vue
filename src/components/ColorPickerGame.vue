<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { colorPickerGame } from "../composables/color-picker.js";



export default {
setup() {
  const colorPicker = colorPickerGame()
return {
  colors: colorPicker.colors,
  message: colorPicker.message,
  matchColor: colorPicker.matchColor,
};
},

};
</script>

<style></style>
