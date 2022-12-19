<template>
  <div class="footer">
    <p>Copyright &copy; {{ getYear() }} Covid-19 Tracker All Right Reserved.</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'FooterModule',
  methods: {
    getYear() {
      return new Date().getFullYear()
    },
  },
})
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.footer {
  padding: 25px;
  background-color: #2d3748;
}

.footer p {
  padding: 5px;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande',
    'Lucida Sans', Arial, sans-serif;
  font-size: 25px;
  color: white;
}
</style>
