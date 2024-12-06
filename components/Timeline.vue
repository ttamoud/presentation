<template>
  <div class="timeline-container h-full flex items-center justify-center">
    <div class="timeline-vertical">
      <div v-for="(item, index) in items" :key="index" 
           class="timeline-item-vertical"
           :style="{ top: `${index * 33}%` }">
        <div class="marker"></div>
        <div class="content-vertical">
          <h3 class="text-lg font-bold">{{ item.title }}</h3>
          <p class="text-sm">{{ item.description }}</p>
        </div>
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
    title: '9 Mois',
    description: 'Déploiement gestion des risques'
  }
]
</script>

<style scoped>
.timeline-container {
  position: relative;
  height: 100%;
  padding: 2rem;
}

.timeline-vertical {
  position: relative;
  height: 100%;
  width: 4px;
  background-color: #2B90B6;
  margin: 0 auto;
}

.timeline-item-vertical {
  position: absolute;
  width: 300px;
  left: 30px;
}

.marker {
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: #2B90B6;
  border: 4px solid #FF9F55;
  border-radius: 50%;
  left: -8px;
  top: 50%;
  transform: translateY(-50%);
}

.content-vertical {
  background-color: rgba(255, 255, 255, 0.1);
  padding: 15px;
  border-radius: 6px;
  margin-left: 20px;
}
</style>