<script setup>
import { Scatter } from 'vue-chartjs'
import { Chart as ChartJS, LinearScale, PointElement, LineElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(LinearScale, PointElement, LineElement, Tooltip, Legend)

const chartData = {
  datasets: [{
    label: 'Recommandations',
    data: [
      { x: 4.5, y: 4.8, r: 25, label: 'Gouvernance' },
      { x: 4.2, y: 4, r: 22, label: 'Contrôles' },
      { x: 3.8, y: 4.2, r: 22, label: 'Performance' },
      { x: 3.5, y: 3.2, r: 20, label: 'RH' },
      { x: 3, y: 3, r: 20, label: 'SI' }
    ],
    backgroundColor: [
      'rgba(255, 99, 132, 0.8)',
      'rgba(54, 162, 235, 0.8)',
      'rgba(255, 206, 86, 0.8)',
      'rgba(75, 192, 192, 0.8)',
      'rgba(153, 102, 255, 0.8)'
    ]
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  scales: {
    x: {
      min: 0,
      max: 5,
      title: {
        display: true,
        text: 'Impact',
        color: '#fff'
      },
      grid: {
        color: 'rgba(255, 255, 255, 0.1)'
      },
      ticks: {
        color: '#fff'
      }
    },
    y: {
      min: 0,
      max: 5,
      title: {
        display: true,
        text: 'Urgence',
        color: '#fff'
      },
      grid: {
        color: 'rgba(255, 255, 255, 0.1)'
      },
      ticks: {
        color: '#fff'
      }
    }
  },
  plugins: {
    tooltip: {
      callbacks: {
        label: function(context) {
          const point = context.raw;
          return [
            `${point.label}`,
            `Impact: ${point.x}`,
            `Urgence: ${point.y}`
          ];
        }
      }
    },
    legend: {
      display: false
    }
  }
}
</script>

<template>
  <div class="h-80">
    <Scatter :data="chartData" :options="chartOptions" />
  </div>
</template>