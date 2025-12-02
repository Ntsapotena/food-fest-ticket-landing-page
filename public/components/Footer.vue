<template>
  <footer class="footer">
    <div class="footer-section">
      <h3 class="footer-title">🎟️ EventHub</h3>
      <p class="footer-text">
        Your place for concerts, festivals, sports, and unforgettable experiences.
      </p>
    </div>

    <div class="footer-section">
      <h4 class="footer-subtitle">📍 Quick Links</h4>
      <ul class="footer-links">
        <li>🏠 Home</li>
        <li>🎫 Events</li>
        <li>📰 News</li>
        <li>📞 Contact Us</li>
      </ul>
    </div>

    <div class="footer-section">
      <h4 class="footer-subtitle">🌐 Follow Us</h4>
      <ul class="footer-links">
        <li>📘 Facebook</li>
        <li>🐦 Twitter</li>
        <li>📸 Instagram</li>
        <li>▶️ YouTube</li>
      </ul>
    </div>

    <div class="footer-bottom">
      <p>© 2025 EventHub. All rights reserved.</p>
    </div>
  </footer>
</template>

<script setup>
// no script needed — component is static
</script>

<style scoped>
.footer {
  background: #111827;
  color: #e5e7eb;
  padding: 40px 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 30px;
  border-top: 4px solid #1f2937;
}

.footer-section {
  flex: 1 1 200px;
}

.footer-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 12px;
  color: #ffffff;
}

.footer-text {
  font-size: 0.95rem;
  color: #d1d5db;
}

.footer-subtitle {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 10px;
  color: #f3f4f6;
}

.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin: 6px 0;
  cursor: pointer;
  transition: 0.2s ease;
}

.footer-links li:hover {
  color: #60a5fa;
  transform: translateX(3px);
}

.footer-bottom {
  width: 100%;
  text-align: center;
  border-top: 1px solid #374151;
  padding-top: 20px;
  margin-top: 20px;
  color: #9ca3af;
  font-size: 0.9rem;
}
</style>
