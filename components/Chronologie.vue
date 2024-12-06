<template>
  <div class="timeline">
    <div class="timeline-line"></div>
    <div v-for="(item, index) in items" :key="index" class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="content">
        <h3 class="text-2xl mb-2">{{ item.title }}</h3>
        <p class="text-lg">{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const items = [
  {
    title: '3 Mois',
    description: 'Mise en place de la gouvernance'
  },
  {
    title: '6 Mois',
    description: 'Contrôles et suivi de performance'
  },
  {
    title: '12 Mois',
    description: 'Déploiement complet'
  }
]
</script>

<style scoped>
.timeline {
  position: relative;
  height: 100%;
  padding: 40px 20px;
  display: flex;
  flex-direction: column;
}

.timeline-line {
  position: absolute;
  width: 3px;
  background-color: #2B90B6;
  top: 38px;
  bottom: 80px;
  left: 51.5px;
}

.timeline-item {
  position: relative;
  margin-bottom: 60px;
  padding-left: 80px;
}

.timeline-dot {
  position: absolute;
  width: 20px;
  height: 20px;
  left: 34px;
  top: 50%;
  transform: translateY(-50%) translateX(-50%);
  background-color: #2B90B6;
  border: 2.5px solid #FF9F55;
  border-radius: 50%;
  z-index: 2;
}

.content {
  background-color: rgba(43, 43, 43, 0.8);
  border-radius: 8px;
  padding: 15px 20px;
  min-width: 250px;
}

h3 {
  color: white;
  margin: 0;
  font-weight: 500;
}

p {
  color: white;
  margin: 0;
  opacity: 0.9;
}
</style>