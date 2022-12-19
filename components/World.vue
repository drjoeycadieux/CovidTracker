<template>
  <div class="world_data">
    <div class="world_boxes">
      <p>Covid-19 Tracker | World Tracker</p>
      <p
        style="font-weight: bold"
        v-for="(WorldData, index) in WorldData"
        :key="WorldData.cases"
      >
        Cases: {{ WorldData.cases }}
      </p>
    </div>
    <div class="world_boxes1">
      <p>Covid-19 Tracker | World Tracker</p>
      <p
        style="font-weight: bold"
        v-for="(WorldData, index) in WorldData"
        :key="WorldData.deaths"
      >
        Deaths: {{ WorldData.deaths }}
      </p>
    </div>
    <div class="time_boxes">
      <p>Last Updated: {{ getTime() }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

import WorldData from '../data/WorldData'

export default Vue.extend({
  name: 'World',
  data() {
    return {
      WorldData: WorldData,
    }
  },
  methods: {
    getTime() {
      return new Date().toUTCString()
    },
  },
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
.world_data {
  padding: 2rem;
  display: block;
  display: flex;
  width: 900px;
  margin: auto;
}

.world_boxes {
  padding: 10px;
  background-color: lightblue;
  border-radius: 10px;
  margin: 8px;
}

.world_boxes p {
  font-size: 25px;
  font-family: sans-serif;
}

.world_boxes1 {
  padding: 10px;
  background-color: firebrick;
  border-radius: 10px;
  margin: 8px;
}

.world_boxes1 p {
  font-size: 25px;
  font-family: sans-serif;
}
.time_boxes {
  padding: 2rem;
  border-radius: 15px;
  border: black solid 1px;
}

.time_boxes p {
  text-align: center;
  font-family: sans-serif;
  font-weight: bold;
}
</style>
