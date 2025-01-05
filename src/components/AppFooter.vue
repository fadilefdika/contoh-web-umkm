<template>
  <v-footer height="auto" class="footer dark-bg">
    <v-container>
      <v-row justify="space-between">
        <!-- Logo dan Sosial Media -->
        <v-col cols="12" md="4" class="text-center text-md-start">
          <div class="brand">
            <img src="@/assets/logo.svg" alt="Logo" class="logo" />
            <p>Dreamy,</p>
          </div>
          <div class="social-links mt-2">
            <a
              v-for="item in socialMedia"
              :key="item.name"
              :href="item.href"
              target="_blank"
              rel="noopener noreferrer"
            >
              <i :class="item.icon" class="social-icon"></i>
            </a>
          </div>
        </v-col>

        <!-- Kontak -->
        <v-col cols="12" md="4" class="text-center text-md-start">
          <h5>Contact Us</h5>
          <p>hello@dreamy.co</p>
          <p>24 Atlantic Ave, Brooklyn, NY 11201</p>
          <p>Dreamy Inc</p>
          <p>+34 875 328 58 47</p>
        </v-col>

        <v-col cols="12" md="4" class="text-center text-md-start">
          <h5 class="mb-2">Subscribe</h5>
          <p class="mb-4">
            Enter your email to get notified about our new solutions
          </p>
          <v-row class="align-center no-gutters">
            <!-- Input Email -->
            <v-col class="pr-2">
              <v-text-field
                v-model="email"
                placeholder="Enter your email"
                variant="outlined"
                density="comfortable"
                hide-details
                outlined
                class="email-input"
              ></v-text-field>
            </v-col>
            <!-- Tombol Subscribe -->
            <v-col cols="auto">
              <v-btn class="subscribe-btn" color="primary" elevation="2">
                <i class="fas fa-paper-plane"></i>
              </v-btn>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-divider class="my-4"></v-divider>
      <v-row>
        <v-col class="text-center text-caption">
          &copy; {{ new Date().getFullYear() }} Dreamy Inc. All rights reserved.
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const socialMedia = [
  { name: "Facebook", icon: "fab fa-facebook-f", href: "https://facebook.com" },
  { name: "Twitter", icon: "fab fa-twitter", href: "https://twitter.com" },
  {
    name: "Instagram",
    icon: "fab fa-instagram",
    href: "https://instagram.com",
  },
];
</script>

<style scoped>
.footer {
  background-color: #1e1e1e;
  color: #ccc;
  padding: 20px 0;
}

.dark-bg {
  background-color: #1e1e1e;
}

.brand {
  display: flex;
  align-items: center;
  gap: 8px;
}

.brand .logo {
  width: 40px;
  height: 40px;
}

.social-links a {
  color: #ccc;
  font-size: 16px;
  margin-right: 12px;
  transition: color 0.3s ease;
}

.social-links a:hover {
  color: #ff4500;
}

.email-input {
  max-width: 200px;
  display: inline-block;
}

.email-input {
  width: 100%;
  border-radius: 4px;
}

.subscribe-btn {
  height: 100%; /* Tombol setinggi input */
  border-radius: 4px;
}
</style>
