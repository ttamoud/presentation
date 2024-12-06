<script setup>
import { Scatter } from 'vue-chartjs'
import { Chart as ChartJS, LinearScale, PointElement, LineElement, Tooltip, Legend } from 'chart.js'

ChartJS.register(LinearScale, PointElement, LineElement, Tooltip, Legend)

const chartData = {
  datasets: [{
    label: 'Recommendations',
    data: [
      { x: 4.5, y: 4.8, r: 15 },
      { x: 4.2, y: 4, r: 12 },
      { x: 3.8, y: 4.2, r: 12 },
      { x: 3.5, y: 3.2, r: 10 },
      { x: 3, y: 3, r: 10 }
    ],
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
  scales: {
    x: {
      min: 0,
      max: 5,
      title: {
        display: true,
        text: 'Impact'
      }
    },
    y: {
      min: 0,
      max: 5,
      title: {
        display: true,
        text: 'Urgency'
      }
    }
  },
  plugins: {
    tooltip: {
      callbacks: {
        label: (context) => {
          const labels = ['Governance', 'Controls', 'Performance', 'Risks', 'SI']
          return labels[context.dataIndex]
        }
      }
    }
  }
}
</script>

<template>
  <div class="h-80">
    <Scatter :data="chartData" :options="chartOptions" />
  </div>
</template>