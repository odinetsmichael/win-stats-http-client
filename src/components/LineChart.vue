<template>
  <Line :data="data" :options="options" />
</template>

<script>
import {
  Chart as ChartJS,
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
} from 'chart.js'
import { Line } from 'vue-chartjs'
import * as chartConfig from './chartConfig.js'

ChartJS.register(
  CategoryScale,
  LinearScale,
  PointElement,
  LineElement,
  Title,
  Tooltip,
  Legend
)

export default {
  name: 'LineChart',
  components: {
    Line
  },
  data() {
    return chartConfig
  }
}
</script>

<style scoped>
  .overwiew{
    display: flex;
    width: 100%;
    height: 300px;
    padding: 50px;
  }
</style>
