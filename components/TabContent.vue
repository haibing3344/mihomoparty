<template>
  <div class="tab-content-container fade-in" :class="{ visible: isVisible }">
    <div class="tab-content-header">
      <h4 class="text-lg font-semibold mb-3">主要特点</h4>
    </div>
    <div class="tab-features">
      <ul class="feature-list">
        <li v-for="(feature, index) in features" :key="index">
          <span class="feature-icon">✓</span>
          <span>{{ feature }}</span>
        </li>
      </ul>
    </div>
    <div v-if="specialOffer" class="special-offer">
      <p class="offer-text">
        <span class="offer-icon">🏷️</span>
        <strong>{{ specialOffer.title }}：</strong> {{ specialOffer.code }}
      </p>
    </div>
    <a :href="actionLink" target="_blank" rel="noopener" class="action-button">
      <span class="button-icon">↗</span> {{ actionText || '访问官网' }}
    </a>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const props = defineProps({
  description: {
    type: String,
    default: ''
  },
  features: {
    type: Array,
    required: true
  },
  specialOffer: {
    type: Object,
    default: null
  },
  actionLink: {
    type: String,
    required: true
  },
  actionText: {
    type: String,
    default: '访问官网'
  }
})

const isVisible = ref(false)

onMounted(() => {
  setTimeout(() => {
    isVisible.value = true
  }, 100)
})
</script>

<style scoped>
.tab-content-container {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.description {
  margin-bottom: 1rem;
  font-size: 0.95rem;
  line-height: 1.5;
}

.tab-features {
  margin-bottom: 1.5rem;
  flex-grow: 1;
}

.feature-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.feature-list li {
  margin-bottom: 0.75rem;
  display: flex;
  gap: 0.5rem;
  align-items: flex-start;
  font-size: 0.9rem;
}

.feature-icon {
  color: var(--vp-c-brand);
  flex-shrink: 0;
}

.special-offer {
  background-color: var(--vp-c-yellow-soft);
  padding: 1rem;
  border-radius: 0.375rem;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

:root.dark .special-offer {
  background-color: rgba(234, 179, 8, 0.2);
}

.offer-text {
  display: flex;
  align-items: flex-start;
  color: var(--vp-c-yellow-dark);
  font-size: 0.9rem;
}

:root.dark .offer-text {
  color: var(--vp-c-yellow);
}

.offer-icon {
  margin-right: 0.5rem;
  flex-shrink: 0;
}

.action-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.625rem 1.5rem;
  border-radius: 0.375rem;
  font-weight: 500;
  background-color: var(--vp-c-brand);
  color: white;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: var(--vp-shadow-1);
  width: 100%;
  text-align: center;
  margin-top: auto;
}

.action-button:hover {
  transform: translateY(-2px);
  box-shadow: var(--vp-shadow-2);
  opacity: 0.9;
}

.button-icon {
  margin-right: 0.5rem;
}

.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>