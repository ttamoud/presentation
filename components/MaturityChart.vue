<script setup>
import { Radar } from 'vue-chartjs'
import { Chart as ChartJS, RadialLinearScale, PointElement, LineElement, Filler, Tooltip, Legend } from 'chart.js'

ChartJS.register(RadialLinearScale, PointElement, LineElement, Filler, Tooltip, Legend)

const chartData = {
  labels: ['Organization', 'Compliance', 'Performance', 'Risk Management', 'Information Systems'],
  datasets: [{
    label: 'Current Maturity',
    data: [2, 2.5, 2, 2.3, 2.2],
    backgroundColor: 'rgba(54, 162, 235, 0.2)',
    borderColor: 'rgb(54, 162, 235)',
    pointBackgroundColor: 'rgb(54, 162, 235)',
    pointBorderColor: '#fff',
    pointHoverBackgroundColor: '#fff',
    pointHoverBorderColor: 'rgb(54, 162, 235)'
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  scales: {
    r: {
      min: 0,
      max: 5,
      ticks: {
        stepSize: 1
      }
    }
  }
}
</script>

<template>
  <div class="h-80">
    <Radar :data="chartData" :options="chartOptions" />
  </div>
</template>