<template>
  <div class="navbar-container">
    <!-- Logo Section -->
    <div class="navbar-logo">
      <img src="/src/assets/logo.svg" alt="Logo" class="logo-img" />
      <span class="brand-name">BrandName</span>
    </div>

    <!-- Navigation Links -->
    <ul class="navbar-links">
      <li v-for="link in links" :key="link.text">
        <a :href="link.route" class="navbar-link">{{ link.text }}</a>
      </li>
    </ul>

    <!-- Mobile Menu Button -->
    <button class="menu-btn" @click="toggleMenu">
      <span v-if="!isMenuOpen">☰</span>
      <span v-else>×</span>
    </button>

    <!-- Mobile Menu -->
    <ul v-if="isMenuOpen" class="mobile-menu">
      <li v-for="link in links" :key="link.text">
        <a :href="link.route" class="navbar-link" @click="toggleMenu">{{
          link.text
        }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      links: [
        { text: "Home", route: "/" },
        { text: "Tentang", route: "/tentangkami" },
        { text: "Produk", route: "/produk" },
      ],
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped>
/* Navbar Container */
.navbar-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 10;
}

/* Logo Section */
.navbar-logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.logo-img {
  max-width: 30px;
  max-height: 30px;
}

.brand-name {
  font-size: 1.25rem;
  font-weight: 500;
  color: #333;
}

/* Navbar Links */
.navbar-links {
  list-style: none;
  display: flex;
  gap: 1.25rem;
  margin: 0;
  padding: 0;
}

.navbar-link {
  font-size: 0.95rem;
  font-weight: 500;
  color: #333;
  text-transform: capitalize;
  text-decoration: none;
  padding: 0.5rem 0.75rem;
  transition: all 0.3s ease;
}

.navbar-link:hover {
  color: #ff4500;
}

/* Mobile Menu */
.menu-btn {
  display: none;
  background: none;
  border: none;
  font-size: 2rem;
  color: #333;
  cursor: pointer;
}

/* Mobile Menu Links */
.mobile-menu {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  position: absolute;
  top: 60px;
  right: 0;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 1rem;
  width: 100%;
  transition: all 0.7s ease;
}

.mobile-menu .navbar-link {
  padding: 1rem;
  text-align: center;
}

/* Responsiveness */
@media (max-width: 960px) {
  .navbar-links {
    display: none;
  }

  .menu-btn {
    display: block;
  }
}
</style>
