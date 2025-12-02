<script>
export default {
  name: "Navbar",
  props: {
    appName: { type: String, default: "My App Vue" },
    links: { 
      type: Array, 
      default: () => [
        { name: "Home", path: "#" },
        { name: "About", path: "#" },
        { name: "Events", path: "#" },
        { name: "Contact", path: "#" }
      ] 
    }
  }
};
</script>

<template>
  <nav class="navbar">
    <div class="brand">{{ appName }}</div>
    <ul class="nav-links">
      <li v-for="link in links" :key="link.name">
        <a :href="link.path">{{ link.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #333;
  color: white;
  padding: 12px 24px;
}
.brand { font-weight: bold; font-size: 1.5rem; }
.nav-links { list-style: none; display: flex; gap: 16px; margin: 0; padding: 0; }
.nav-links a { color: white; text-decoration: none; }
.nav-links a:hover { text-decoration: underline; }
</style>
