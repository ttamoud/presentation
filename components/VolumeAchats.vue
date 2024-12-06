<script setup>
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend } from 'chart.js'

ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend)

const chartData = {
  labels: ['SI', 'Services Généraux', 'Pharmacie', 'RH'],
  datasets: [{
    label: 'Volume d\'achats (M€)',
    data: [15, 20, 25, 5],
    backgroundColor: ['rgba(75, 192, 192, 0.6)', 'rgba(54, 162, 235, 0.6)', 'rgba(153, 102, 255, 0.6)', 'rgba(255, 159, 64, 0.6)']
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  plugins: {
    legend: {
      position: 'top',
      labels: {
        color: 'white'
      }
    },
    title: {
      display: true,
      text: 'Volume d\'achats par service',
      color: 'white'
    }
  },
  scales: {
    x: {
      ticks: {
        color: 'white',
        font: {
          size: 11
        },
        maxRotation: 0,
        autoSkip: false,
        padding: 5
      },
      grid: {
        color: 'rgba(255, 255, 255, 0.1)'
      }
    },
    y: {
      ticks: {
        color: 'white'
      },
      grid: {
        color: 'rgba(255, 255, 255, 0.1)'
      }
    }
  }
}
</script>

<template>
  <div class="h-80">
    <Bar :data="chartData" :options="chartOptions" />
  </div>
</template>