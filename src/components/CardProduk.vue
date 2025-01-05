<template>
  <v-col :cols="cols" :sm="sm">
    <v-card class="mx-auto" max-width="390">
      <!-- Gambar -->
      <v-img class="align-end text-white" height="200" :src="imageSrc" cover>
      </v-img>

      <!-- Judul -->
      <v-card-title>{{ title }}</v-card-title>

      <!-- Deskripsi -->
      <v-card-text>
        <div class="truncate-text">
          {{ description }}
        </div>
      </v-card-text>

      <!-- Tombol -->
      <v-card-actions>
        <v-btn color="orange" text @click="onOrderClick">Pesan Sekarang</v-btn>
      </v-card-actions>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "CardProduk",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    imageSrc: {
      type: String,
      required: true,
    },
    cols: {
      type: Number,
      default: 12,
    },
    sm: {
      type: Number,
      default: 4,
    },
  },
  methods: {
    onOrderClick() {
      this.$emit("order-click");
    },
  },
};
</script>

<style scoped>
/* Membatasi teks maksimal 3 baris */
.truncate-text {
  display: -webkit-box;
  -webkit-line-clamp: 3; /* Maksimal 3 baris */
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  min-height: 4.5em; /* Mengunci tinggi area untuk 3 baris */
  line-height: 1.5em; /* Jarak antar baris */
}
</style>
