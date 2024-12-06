<script setup>
import { Doughnut } from 'vue-chartjs'
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(ArcElement, Tooltip, Legend)

const chartData = {
  labels: ['Gouvernance', 'Contrôles', 'Performance', 'Risques', 'SI'],
  datasets: [{
    data: [15, 25, 30, 20, 60],
    backgroundColor: [
      'rgba(255, 99, 132, 0.6)',
      'rgba(54, 162, 235, 0.6)',
      'rgba(255, 206, 86, 0.6)',
      'rgba(75, 192, 192, 0.6)',
      'rgba(153, 102, 255, 0.6)'
    ]
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  plugins: {
    legend: {
      position: 'right'
    },
    tooltip: {
      callbacks: {
        label: (context) => {
          return `${context.label}: ${context.raw}k€`
        }
      }
    }
  }
}
</script>

<template>
  <div class="h-80">
    <Doughnut :data="chartData" :options="chartOptions" />
  </div>
</template>