---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: slide-left
title: Rapport d'Audit - Fonction Achats
mdc: true
---

# Rapport d'Audit
## Fonction Achats - Fondation Santé Service

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Appuyez sur Espace pour la suite <carbon:arrow-right class="inline"/>
  </span>
</div>

---
transition: fade-out
layout: two-cols
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }">

# Contexte de l'Audit

</div>

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 400 } }" class="mt-12 text-lg">
 
- Volume : 65M€ d'achats annuels
- Périmètre : 4 services
  - Systèmes d'Information
  - Services Généraux
  - Pharmacie
  - Ressources Humaines
- Période : 2021-2022

</div>

::right::

<div v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800, delay: 800 } }">
  <VolumeAchats class="mt-12"/>
</div>

---
layout: two-cols
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }">

# Constats Principaux

<div class="pr-8 space-y-8 text-sm">
  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 400 } }">
    <h4 class="text-lg mb-4">Points Forts</h4>
    <ul class="list-disc pl-4">
      <li>Expertise technique</li>
      <li>Engagement de la direction</li>
      <li>Base fournisseurs diversifiée</li>
      <li>Outils de base en place</li>
    </ul>
  </div>

  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 800 } }">
    <h4 class="text-lg mb-4">Axes d'Amélioration</h4>
    <ul class="list-disc pl-4">
      <li>Optimisation de l'organisation</li>
      <li>Formalisation des processus requise</li>
      <li>Clarification des rôles à effectuer</li>
      <li>Renforcement des contrôles</li>
    </ul>
  </div>
</div>
</div>

::right::

<div v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800, delay: 1200 } }">
  <GrapheMaturite class="mt-12"/>
</div>

---
layout: section
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }" v-motion-fade-out>

# Recommandations

</div>

---
layout: two-cols
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }">

# Actions Prioritaires

<div class="pr-8 space-y-8 text-sm">
  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 400 } }">
    <h4 class="text-lg mb-4">1. Renforcer la gouvernance</h4>
    <ul class="list-disc pl-4">
      <li>Créer un comité achats mensuel</li>
      <li>Formaliser les processus</li>
      <li>Clarifier les rôles</li>
    </ul>
  </div>

  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 800 } }">
    <h4 class="text-lg mb-4">2. Améliorer les contrôles</h4>
    <ul class="list-disc pl-4">
      <li>Former les acteurs</li>
      <li>Mettre en place des points de contrôle</li>
      <li>Simplifier les procédures</li>
    </ul>
  </div>

  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 1200 } }">
    <h4 class="text-lg mb-4">3. Piloter la performance</h4>
    <ul class="list-disc pl-4">
      <li>Définir les indicateurs</li>
      <li>Déployer les outils de suivi</li>
      <li>Fixer les objectifs annuels</li>
    </ul>
  </div>
</div>
</div>

::right::

<div v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800, delay: 1600 } }">
  <MatricePriorite class="mt-12"/>
</div>

---
layout: two-cols
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }">

# Allocation Budgétaire

<div class="mt-20 text-sm pr-8">
  <h3 class="font-bold mb-2">Répartition du Budget</h3>
  <p class="mb-2">Le budget total de 150k€ est réparti stratégiquement pour maximiser l'impact des améliorations:</p>
  <ul class="list-disc pl-4">
    <li>Priorité sur l'optimisation SI (60k€)</li>
    <li>Investissement équilibré dans les contrôles et la performance</li>
  </ul>
</div>
</div>

::right::

<div v-motion :initial="{ x: 50, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800, delay: 400 } }">
  <GrapheBudget class="mt-12"/>
</div>

---
layout: two-cols
---

<div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800 } }">

# Calendrier de mise en oeuvre

<div class="pr-8 space-y-4 text-sm">
  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 400 } }">
    <h4 class="text-lg mb-2">Court Terme (3 mois)</h4>
    <ul class="list-disc pl-4">
      <li>Structure de gouvernance</li>
      <li>Formation des équipes</li>
      <li>Mise en place des KPIs</li>
    </ul>
  </div>

  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 800 } }">
    <h4 class="text-lg mb-2">Moyen Terme (6 mois)</h4>
    <ul class="list-disc pl-4">
      <li>Déploiement des outils</li>
      <li>Optimisation des processus</li>
      <li>Renforcement des contrôles</li>
    </ul>
  </div>

  <div v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 800, delay: 1200 } }">
    <h4 class="text-lg mb-2">Long Terme (12 mois)</h4>
    <ul class="list-disc pl-4">
      <li>Automatisation avancée</li>
      <li>Extension du périmètre</li>
      <li>Revue de performance</li>
    </ul>
  </div>
</div>
</div>

::right::

<div v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800, delay: 1600 } }">
  <Chronologie class="mt-12"/>
</div>

---
layout: center
class: text-center
---

# Merci de votre attention 

[Contacter l'Équipe](mailto:ttamoud1@myges.fr)