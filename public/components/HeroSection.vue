<script setup>
import { defineProps, computed } from 'vue';

// 1. Define Props (Inputs for the component)
const props = defineProps({
  title: {
    type: String,
    required: true,
    default: 'Welcome to Our Site',
  },
  subtitle: {
    type: String,
    default: 'Discover amazing things with us.',
  },
  ctaText: { // CTA: Call to Action
    type: String,
    default: 'Get Started',
  },
  imageSrc: {
    type: String,
    default: 'path/to/default/hero-image.jpg',
  },
});

// 2. Define Computed Properties (Derived values)
// A computed property for a background style is useful for dynamic components.
const backgroundStyle = computed(() => {
  return {
    backgroundImage: `url(${props.imageSrc})`,
  };
});

// 3. Define Emits (Events the component can send out)
const emit = defineEmits(['cta-click']);

// 4. Define Component Methods
const handleCtaClick = () => {
  // Emit an event when the CTA button is clicked
  emit('cta-click');
  console.log('CTA Clicked!');
};
</script>

<template>
  <section class="hero-section">
    <div class="hero-overlay"></div>

    <div class="hero-content">
      <h1 class="hero-title">{{ title }}</h1>
      
      <p class="hero-subtitle">{{ subtitle }}</p>
      
      <button class="hero-cta-button" @click="handleCtaClick">
        {{ ctaText }}
      </button>
    </div>
  </section>
</template>

<style scoped>
/* Scoped styles ensure they only apply to this component */
.hero-section {
  background-image: url("https://images.pexels.com/photos/1763067/pexels-photo-1763067.jpeg");
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 70vh; /* A good height for a hero section */
  background-size: cover;
  background-position: center;
  position: relative;
  color: white; /* Default text color */
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.4); /* Dark semi-transparent overlay */
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  text-align: center;
  max-width: 800px;
  padding: 20px;
}

.hero-title {
  font-size: 3.5rem;
  margin-bottom: 0.5rem;
}

.hero-subtitle {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
}

.hero-cta-button {
  padding: 12px 30px;
  font-size: 1.1rem;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background-color: #42b883; /* Vue Green */
  color: white;
  transition: background-color 0.3s;
}

.hero-cta-button:hover {
  background-color: #33a06f;
}
</style>