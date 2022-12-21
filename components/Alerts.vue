<template>
  <div class="alerts">
    <p>
      For the most up to date information regarding COVID-19 in Canada, please
      consult
      <a
        href="https://www.canada.ca/en/public-health/services/diseases/coronavirus-disease-covid-19.html"
        >Canada Deptartment of Health</a
      >. This site should not be used for life saving information - instead,
      rather, a source for numbers and statistics.
    </p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Alerts',
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.alerts {
  padding: 2rem;
  background-color: dodgerblue;
  width: 900px;
  margin: auto;
  border-radius: 15px;
}

.alerts p {
  font-family: sans-serif;
  text-align: center;
  font-size: 15px;
  color: black;
  font-weight: bold;
}

.alerts a {
  color: white;
  font-family: 'Courier New', Courier, monospace;
}

.alerts a:hover {
  color: lightslategray;
}
</style>
