<template>
  <div id="app">
    <canvas ref="canvas" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { Line, Bar, Radar, PolarArea, Bubble, Scatter, Doughnut  } from 'vue-chartjs';

@Component({
  extends: Bubble,
})
export default class App extends Vue {
  mounted () {
    this.renderChart({
      labels: ['A', 'B', 'C', 'D', 'E'],
      datasets: [
        {
          label: 'Stas lox',
          backgroundColor: ['#f87979', 'red', 'green', 'blue', 'purple'],
          borderColor: [ 'purple', 'blue', 'red', 'green', '#f87979'],
          fill: false,
          borderWidth: 3,
          data: [5,4,5,6,7],
          // data: [{
          //   x: 20,
          //   y: 30,
          //   r: 15
          // }, {
          //   x: 40,
          //   y: 10,
          //   r: 10
          // }], for Bubble, Scatter
        }
      ]
    })
  }
}
</script>

<style lang="scss">
#app {
  position: relative;
  width: 400px;
  height: 340px;
}
</style>
