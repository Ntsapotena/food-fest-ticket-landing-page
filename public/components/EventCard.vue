<template>
  <div class="event-list">
    <div 
      v-for="(event, i) in events" 
      :key="i" 
      class="event-card"
    >
      <img :src="event.image" class="event-image" />

      <div class="event-info">
        <h3 class="event-title">{{ event.title }}</h3>
        <p class="event-venue">{{ event.venue }}</p>
        <p class="event-date">{{ event.date }}</p>
        <p class="event-description">{{ event.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const events = [
  {
    title: "Summer Music Festival",
    venue: "City Park Arena",
    date: "July 14, 2025",
    description: "Live performances from top artists all night.",
    image: "https://images.pexels.com/photos/1684187/pexels-photo-1684187.jpeg"
  },
  {
    title: "Contemporary Art Exhibition",
    venue: "Modern Art Gallery",
    date: "August 22, 2025",
    description: "A showcase of modern artworks from global creators.",
    image: "https://images.pexels.com/photos/1190298/pexels-photo-1190298.jpeg"
  },
  {
    title: "Tech Innovators Conference",
    venue: "International Expo Center",
    date: "September 3, 2025",
    description: "Discover upcoming technology trends and keynote speakers.",
    image: "https://images.pexels.com/photos/1763075/pexels-photo-1763075.jpeg"
  },
  {
    title: "Outdoor Adventure Day",
    venue: "Highland Nature Trail",
    date: "October 5, 2025",
    description: "Hiking, exploration, and a guided nature challenge.",
    image: "https://images.pexels.com/photos/713644/pexels-photo-713644.jpeg"
  }
];
</script>

<style scoped>
.event-list {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 20px;
}

.event-card {
  display: flex;
  gap: 15px;
  background: #ffffff;
  padding: 14px;
  border-radius: 12px;
  box-shadow: 0px 4px 14px rgba(0,0,0,0.12);
  transition: 0.2s ease;
  cursor: pointer;
}

.event-card:hover {
  transform: translateY(-4px);
  box-shadow: 0px 6px 20px rgba(0,0,0,0.15);
}

.event-image {
  width: 140px;
  height: 140px;
  object-fit: cover;
  border-radius: 8px;
}

.event-info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.event-title {
  margin: 0;
  font-size: 1.2rem;
  font-weight: 700;
}

.event-venue {
  font-size: 0.95rem;
  color: #666;
}

.event-date {
  color: #1d63f0;
  font-weight: 600;
  margin: 6px 0;
}

.event-description {
  font-size: 0.9rem;
  color: #444;
}
</style>
