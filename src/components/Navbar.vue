<template>
  <v-app-bar app color="white" flat class="navbar">
    <v-container>
      <v-row align="center" justify="space-between" class="navbar-container">
        <!-- Logo -->
        <v-row align="center" class="navbar-logo">
          <v-img
            src="/src/assets/logo.svg"
            alt="Logo"
            max-width="30"
            max-height="30"
            contain
            class="me-2"
          ></v-img>
          <span class="text-h6 font-weight-medium">BrandName</span>
        </v-row>

        <!-- Navigation Links -->
        <v-row tag="ul" class="navbar-links">
          <li v-for="link in links" :key="link.text">
            <v-btn :to="link.route" text exact class="navbar-link">
              {{ link.text }}
            </v-btn>
          </li>
        </v-row>
      </v-row>
    </v-container>
  </v-app-bar>
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
    };
  },
};
</script>

<style scoped>
/* Navbar */
.navbar {
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Navbar Logo */
.navbar-logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.navbar-logo span {
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
  transition: all 0.3s ease;
  padding: 0.5rem 0.75rem;
}

.navbar-link:hover {
  color: #ff4500;
}

/* Responsiveness */
@media (max-width: 768px) {
  .navbar-links {
    display: none; /* Bisa diganti dengan toggle menu */
  }
}
</style>
