<template>
  <div id="app">
    <line-chart
        :data="{'2017-01-01': 11, '2017-01-02': 6}"
        :colors="['#b00', '#666']"
        width="600px"
        height="400px"
    />
    <pie-chart
        :data="[['Blueberry', 44], ['Strawberry', 23], ['Stas', 47]]"
        :colors="['#060728', '#bd0d0d', 'purple']"
        width="600px"
        height="400px"
        :donut="true"
    />
    <column-chart
        :data="[['Sun', 32], ['Mon', 46], ['Tue', 28]]"
        width="600px"
        height="400px"
    />
    <bar-chart
        :data="[['Work', 32], ['Play', 1492]]"
        width="600px"
        height="400px"
    />
    <area-chart
        :data="{'2017-01-01': 11, '2017-01-02': 6}"
        width="600px"
        height="400px"
    />
    <scatter-chart
        :data="[[174.0, 80.0], [176.5, 82.3]]"
        xtitle="Size"
        ytitle="Population"
        width="600px"
        height="400px"
    />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
