<template>
  <v-app-bar app color="white" flat class="navbar">
    <v-container>
      <v-row align="center" justify="space-between" class="navbar-container">
        <!-- Logo -->
        <v-row align="center" class="navbar-logo">
          <v-img
            src="/src/assets/logo.svg"
            alt="Logo"
            max-width="40"
            max-height="40"
            contain
            class="me-2"
          ></v-img>
          <span class="text-h5 font-weight-bold">BrandName</span>
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
        { text: "Tentang Kami", route: "/tentangkami" },
        { text: "Produk", route: "/produk" },
      ],
    };
  },
};
</script>

<style scoped>
/* Navbar Container */
.navbar {
  position: sticky;
  width: 100%;
  padding: 0.5rem 0;
}

/* Navbar Logo */
.navbar-logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.navbar-logo span {
  font-size: 1.5rem;
  font-weight: bold;
  color: #333;
}

/* Navbar Links */
.navbar-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}

.navbar-link {
  font-size: 1rem;
  font-weight: 500;
  color: #333;
  text-transform: capitalize;
  transition: color 0.3s ease-in-out;
}

.navbar-link:hover {
  color: #ff4500;
}
</style>
