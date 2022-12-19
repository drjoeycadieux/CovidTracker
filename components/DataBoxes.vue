<template>
  <div class="data_boxes">
    <p id="time">Last Updated: {{ getTime() }}</p>
    <!-- data_boxes -->
    <div class="boxes1">
      <p>Covid-19 Tracker - Data Tracker</p>
      <h1
        class="cases_data"
        v-for="(CovidMtl, index) in CovidMtl"
        :key="CovidMtl.cases"
      >
        Cases: {{ CovidMtl.cases }}
      </h1>
    </div>
    <div class="boxes2">
      <p>Covid-19 Tracker - Data Tracker</p>
      <h1
        class="cases_data"
        v-for="(CovidMtl, index) in CovidMtl"
        :key="CovidMtl.deaths"
      >
        Deaths: {{ CovidMtl.deaths }}
      </h1>
    </div>
    <div class="boxes3">
      <p>Covid-19 Tracker - Data Tracker</p>
      <h1
        class="cases_data"
        v-for="(CovidMtl, index) in CovidMtl"
        :key="CovidMtl.recoveries"
      >
        Recoveries: {{ CovidMtl.recoveries }}
      </h1>
    </div>
    <div class="boxes4">
      <p>Covid-19 Tracker - Data Tracker</p>
      <h1
        class="cases_data"
        v-for="(CovidMtl, index) in CovidMtl"
        :key="CovidMtl.hospitalized"
      >
        Hospitalized: {{ CovidMtl.hospitalized }}
      </h1>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import moment from 'moment'

import CovidMtl from '../data/CovidMtl.js'

export default Vue.extend({
  name: 'DataBoxes',
  data() {
    return {
      CovidMtl: CovidMtl,
    }
  },
  methods: {
    getTime() {
      return moment().format('LTS')
    },
  },
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.data_boxes {
  padding: 2rem;
  display: block;
  display: flex;
  width: 900px;
  margin: auto;
}

.boxes1 {
  padding: 10px;
  background-color: lightblue;
  border-radius: 10px;
  margin: 8px;
}

.boxes1 p {
  font-size: 25px;
  font-family: sans-serif;
}

.cases_data {
  font-family: sans-serif;
  font-size: 25px;
  text-align: center;
}

.boxes2 {
  padding: 10px;
  background-color: firebrick;
  border-radius: 10px;
  margin: 8px;
}

.boxes2 p {
  font-size: 25px;
  font-family: sans-serif;
}

.boxes3 {
  padding: 10px;
  background-color: lightgreen;
  border-radius: 10px;
  margin: 8px;
}

.boxes3 p {
  font-size: 25px;
  font-family: sans-serif;
}

.boxes4 {
  padding: 10px;
  background-color: violet;
  border-radius: 10px;
  margin: 8px;
}

.boxes4 p {
  font-size: 25px;
  font-family: sans-serif;
}
#time {
  font-family: sans-serif;
  font-weight: bold;
  border: solid 1px black;
  padding: 2rem;
  text-align: center;
  font-size: 25px;
  border-radius: 15px;
}
</style>
