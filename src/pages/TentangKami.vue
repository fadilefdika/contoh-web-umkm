<template>
  <v-container fluid class="about-section py-12 px-4">
    <v-row
      align="center"
      justify="space-between"
      class="mx-auto"
      style="max-width: 1440px"
    >
      <!-- Image Section -->
      <v-col cols="12" md="6">
        <v-img
          src="../assets/contoh.jpg"
          alt="CEO Perusahaan"
          max-width="90%"
          class="rounded-xl elevation-3 image-hover"
          :aspect-ratio="4 / 3"
          cover
        >
          <template v-slot:placeholder>
            <v-progress-circular
              indeterminate
              color="#ff4500"
              size="24"
            ></v-progress-circular>
          </template>
        </v-img>
      </v-col>

      <!-- Content Section -->
      <v-col cols="12" md="6">
        <div class="content-wrapper">
          <!-- Header Section -->
          <div class="mb-6">
            <h2 class="text-h3 font-weight-bold gradient-text mb-2">
              Tentang Kami
            </h2>
            <v-divider
              class="primary mb-4"
              style="width: 60px; height: 4px"
            ></v-divider>
          </div>

          <!-- Main Content -->
          <p class="text-body-1 text-dark-gray mb-6">
            Kami adalah perusahaan yang berkomitmen untuk menyediakan produk
            ayam berkualitas tinggi. Semua ayam diproses secara higienis dengan
            standar terbaik untuk memenuhi kebutuhan pelanggan di seluruh
            Indonesia hingga mancanegara.
          </p>

          <!-- Vision Statement -->
          <v-card
            class="vision-card mb-6 pa-6"
            elevation="0"
            color="rgba(255, 69, 0, 0.1)"
          >
            <v-icon class="mb-4" size="32" color="#ff4500"
              >mdi-lightbulb</v-icon
            >
            <p class="text-h6 font-italic" style="color: #ff4500">
              "Visi kami adalah memberikan layanan terbaik kepada pelanggan
              kami, menyediakan produk berkualitas tinggi yang mendukung
              kebutuhan hidup sehat."
            </p>
          </v-card>

          <!-- CEO Quote -->
          <div class="ceo-signature">
            <div>
              <p class="text-h6 font-weight-bold text-dark-gray mb-1">
                Nama CEO
              </p>
              <p class="text-subtitle-2 text-dark-gray">CEO & Pendiri</p>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "AboutSection",
  mounted() {
    // Add any mounted logic if needed
  },
};
</script>

<style scoped>
.about-section {
  background: #f8f9fa;
}

.image-hover {
  transition: transform 0.3s ease-in-out;
}

.image-hover:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.content-wrapper {
  padding: 2rem;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(10px);
  border-radius: 16px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
}

.gradient-text {
  background: linear-gradient(45deg, #ff4500, #ff6347);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.vision-card {
  border-left: 4px solid #ff4500;
  transition: transform 0.3s ease;
}

.vision-card:hover {
  transform: translateX(6px);
}

.ceo-signature {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  border-radius: 12px;
  background: #f1f3f5;
}

.text-dark-gray {
  color: #555555;
}

/* Responsive Design */
@media (max-width: 960px) {
  .content-wrapper {
    padding: 1.5rem;
  }

  .gradient-text {
    font-size: 1.875rem !important;
  }
}
</style>
