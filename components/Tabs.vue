<template>
  <div class="cards-container">
    <div class="cards-grid">
      <div
        v-for="(tab, index) in tabs"
        :key="index"
        class="card fade-in"
        :style="{ animationDelay: `${index * 0.1}s` }"
      >
        <div class="card-header" :style="{ backgroundColor: tab.color }">
          <h3 class="card-title">{{ tab.title }}</h3>
          <p class="card-subtitle">{{ tab.subtitle }}</p>
        </div>
        <div class="card-content">
          <slot :name="`tab-${index}`"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  tabs: {
    type: Array,
    required: true
  }
})
</script>

<style scoped>
.cards-container {
  margin-bottom: 2rem;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.5rem;
}

.card {
  border-radius: 0.5rem;
  overflow: hidden;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  height: 100%;
  box-shadow: var(--vp-shadow-2);
  background-color: var(--vp-c-bg);
  display: flex;
  flex-direction: column;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: var(--vp-shadow-4);
}

.card-header {
  padding: 1.5rem;
  color: white;
  position: relative;
}

.card-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.2), transparent);
  z-index: 0;
}

.card-title {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  position: relative;
  z-index: 1;
}

.card-subtitle {
  opacity: 0.9;
  position: relative;
  z-index: 1;
}

.card-content {
  padding: 1.5rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.fade-in {
  opacity: 0;
  animation: fadeIn 0.6s ease forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .cards-grid {
    grid-template-columns: 1fr;
  }
}
</style>