<template>
  <v-container class="our-services-section" fluid>
    <div class="text-center mb-10">
      <h2 class="section-title">Layanan Kami</h2>
      <p class="section-description">
        Kami menyediakan berbagai layanan berkualitas untuk memenuhi kebutuhan
        Anda.
      </p>
    </div>
    <v-row justify="center">
      <v-col cols="12" sm="4" md="3" class="service-item text-center">
        <i class="fas fa-utensils service-icon"></i>
        <h3 class="service-title">Kuliner Berkualitas</h3>
        <p class="service-description">
          Menyediakan berbagai pilihan makanan berkualitas dengan cita rasa
          terbaik.
        </p>
      </v-col>
      <v-col cols="12" sm="4" md="3" class="service-item text-center">
        <i class="fas fa-leaf service-icon"></i>
        <h3 class="service-title">Bahan Alami</h3>
        <p class="service-description">
          Menggunakan bahan alami yang segar dan sehat dalam setiap produk kami.
        </p>
      </v-col>
      <v-col cols="12" sm="4" md="3" class="service-item text-center">
        <i class="fas fa-shipping-fast service-icon"></i>
        <h3 class="service-title">Pengiriman Cepat</h3>
        <p class="service-description">
          Layanan pengiriman cepat untuk memastikan pesanan Anda sampai tepat
          waktu.
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "OurServices",
};
</script>

<style scoped>
.our-services-section {
  background-color: #fff;
  padding: 40px 20px;
}

.section-title {
  font-size: 2rem;
  font-weight: bold;
  color: #333;
}

.section-description {
  font-size: 1rem;
  color: #555;
  max-width: 600px;
  margin: 0 auto;
}

.service-item {
  margin-bottom: 20px;
}

.service-icon {
  font-size: 48px;
  color: #ff4500;
  margin-bottom: 10px;
}

.service-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #333;
  margin-top: 10px;
}

.service-description {
  font-size: 0.9rem;
  color: #666;
}
</style>
