<template>
  <div class="header_module">
    <p v-for="(textField, index) in TextData" :key="textField">
      {{ textField.header_text }}
    </p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

import TextData from '../data/TextData'

export default Vue.extend({
  name: 'HeaderModule',
  data() {
    return {
      TextData: TextData,
    }
  },
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.header_module {
  padding: 150px;
  background-color: #2d3748;
}

.header_module h3 {
  color: lightslategray;
  text-align: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.header_module p {
  padding: 1px;
  color: white;
  font-size: 70px;
  font-family: sans-serif;
  text-align: center;
}
</style>
