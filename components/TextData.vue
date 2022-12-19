<template>
  <div class="text_data">
    <h1 v-for="(textField, index) in textField" :key="textField">
      {{ textField.title }}
    </h1>
  </div>
</template>

<script>
import Vue from 'vue'

import textField from '../data/TextData'

export default Vue.extend({
  name: 'TextData',
  data() {
    return {
      textField: textField,
    }
  },
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.text_data {
  padding: 15px;
  border: solid black 1px;
  border-radius: 15px;
  width: 800px;
  margin: auto;
  text-align: center;
}

.text_data h1 {
  font-weight: bold;
  color: black;
  font-family: sans-serif;
}
</style>
