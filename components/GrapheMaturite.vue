<script setup>
import { Radar } from 'vue-chartjs'
import { Chart as ChartJS, RadialLinearScale, PointElement, LineElement, Filler, Tooltip, Legend } from 'chart.js'

ChartJS.register(RadialLinearScale, PointElement, LineElement, Filler, Tooltip, Legend)

const chartData = {
  labels: ['Organisation', 'Conformité', 'Performance', 'Gestion des Risques', 'Systèmes d\'Information'],
  datasets: [{
    label: 'Maturité Actuelle',
    data: [2, 2.5, 2, 2.3, 2.2],
    backgroundColor: 'rgba(54, 162, 235, 0.3)',
    borderColor: 'rgb(54, 162, 235)',
    borderWidth: 2,
    pointBackgroundColor: 'rgb(54, 162, 235)',
    pointBorderColor: '#fff',
    pointHoverBackgroundColor: '#fff',
    pointHoverBorderColor: 'rgb(54, 162, 235)',
    pointRadius: 4
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
        stepSize: 1,
        color: 'rgba(255, 255, 255, 0.7)',
        backdropColor: 'transparent'
      },
      grid: {
        color: 'rgba(255, 255, 255, 0.1)'
      },
      angleLines: {
        color: 'rgba(255, 255, 255, 0.1)'
      },
      pointLabels: {
        color: 'rgba(255, 255, 255, 0.9)',
        font: {
          size: 12
        }
      }
    }
  },
  plugins: {
    legend: {
      labels: {
        color: 'rgba(255, 255, 255, 0.9)'
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