<template>
  <div id="app">
    <chart :type="'pie'" :data="data" :options="options"></chart>
  </div>
</template>

<script>
import Chart from 'vue-bulma-chartjs'

export default {
  components: {
    Chart
  },

  data () {
    return {
      data: {
        labels: ['Sleeping', 'Designing', 'Coding', 'Cycling'],
        datasets: [
          {
            data: [20, 40, 5, 35],
            backgroundColor: [
              '#1fc8db',
              '#fce473',
              '#42afe3',
              '#ed6c63',
              '#97cd76'
            ]
          }
        ]
      },
      options: {
        segmentShowStroke: false
      }
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
