<template>
  <v-container class="hero bg-white" fluid>
    <div class="text-content">
      <h1 class="text-center">Produk Kami</h1>
    </div>
    <v-row justify="center" align="center" class="pa-4">
      <CardProduk
        v-for="(product, index) in products"
        :key="index"
        :title="product.title"
        :description="product.description"
        :imageSrc="product.imageSrc"
        @order-click="handleOrderClick"
      />
    </v-row>
  </v-container>
</template>

<script>
import AyamCabeIjo from "@/assets/products/ayam-cabe-ijo.jpg";
import AyamKuning from "@/assets/products/ayam-kuning.jpg";
import SateAyam from "@/assets/products/sate-ayam.jpg";

export default {
  name: "Produk",
  data() {
    return {
      products: [
        {
          title: "Ayam Cabe Ijo",
          description: "Nikmati kelezatan ayam dengan bumbu cabe ijo khas.",
          imageSrc: AyamCabeIjo,
        },
        {
          title: "Ayam Kuning",
          description: "Ayam berbumbu kuning yang lezat dan bergizi.",
          imageSrc: AyamKuning,
        },
        {
          title: "Sate Ayam",
          description: "Sate ayam dengan bumbu kacang khas Indonesia.",
          imageSrc: SateAyam,
        },
      ],
    };
  },
  methods: {
    handleOrderClick() {
      alert("Pesan Sekarang clicked");
    },
  },
};
</script>

<style scoped>
.text-content {
  color: #333;
  padding: 10px 0;
}
</style>
