<template lang="pug">
  .container
    h1 Top
    vue-apex-charts(width="500" type="bar" :options="options" :series="series")
</template>

<script>
import VueApexCharts from 'vue-apexcharts'

export default {
  name: 'Top',
  components: {
    VueApexCharts
  },
  data () {
    return {
      options: {
        chart: {
          id: 'vuechart-example'
        },
        xaxis: {
          categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998]
        }
      },
      series: [{
        name: 'series-1',
        data: [30, 40, 45, 50, 49, 60, 70, 91]
      }]
    }
  }
};
</script>

<style scoped>
.container {
  margin: 24px;
}
</style>
