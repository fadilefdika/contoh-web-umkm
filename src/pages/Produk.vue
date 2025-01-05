<template>
  <v-container class="hero bg-white py-12" fluid>
    <div class="text-center mb-8">
      <h1 class="text-h3 font-weight-bold">Produk Kami</h1>
      <p class="text-body-1 text-grey-darken-2">
        Nikmati berbagai pilihan menu ayam lezat dan bergizi.
      </p>
    </div>

    <!-- Kolom untuk Grid Produk -->
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
import AyamTaliwang from "@/assets/products/ayam-taliwang.jpg";
import SemurAyam from "@/assets/products/semur-ayam.jpg";
import AyamPanggang from "@/assets/products/ayam-panggang.jpg";
import AyamBBQ from "@/assets/products/ayam-bbq.jpg";

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
        {
          title: "Ayam Taliwang",
          description: "Ayam bakar khas Lombok dengan bumbu pedas.",
          imageSrc: AyamTaliwang,
        },
        {
          title: "Semur Ayam",
          description: "Ayam dengan bumbu semur yang kaya rasa.",
          imageSrc: SemurAyam,
        },
        {
          title: "Ayam Panggang",
          description: "Ayam panggang dengan bumbu pilihan yang nikmat.",
          imageSrc: AyamPanggang,
        },
        {
          title: "Ayam BBQ",
          description: "Ayam dengan rasa BBQ yang menggugah selera.",
          imageSrc: AyamBBQ,
        },
      ],
    };
  },
  methods: {
    handleOrderClick(product) {
      alert(`Pesan Sekarang untuk ${product.title}`);
    },
  },
};
</script>

<style scoped>
.hero {
  background-color: #f9f9f9;
}

.text-center {
  text-align: center;
}

.v-row {
  gap: 24px;
}

.v-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.v-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.v-img {
  object-fit: cover;
}

.v-card-title {
  font-weight: bold;
}

.v-btn {
  width: 100%;
}
</style>
