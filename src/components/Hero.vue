<template>
  <v-container class="hero" fluid>
    <v-row align="center" justify="space-between">
      <!-- Text Content Section -->
      <v-col cols="12" md="6" class="text-content">
        <h1>
          Rasakan Lezatnya <br />
          <span>Hidangan Ayam</span>
        </h1>
        <p>
          Temukan berbagai varian ayam berkualitas tinggi yang siap memanjakan
          lidah Anda. Dari ayam panggang yang menggoda hingga ayam taliwang yang
          otentik, semuanya tersedia untuk Anda.
        </p>
        <v-btn color="orange" class="cta-button" large>Pesan Sekarang</v-btn>
      </v-col>

      <!-- Image Content Section -->
      <v-col cols="12" md="6" class="image-content">
        <div class="image-wrapper-one">
          <!-- Gambar 1 -->
          <v-img
            class="food-image-one"
            src="../assets/products/ayam-panggang.jpg"
            alt="ayam panggang"
          />
        </div>
        <div class="image-wrapper-two">
          <!-- Gambar 2 -->
          <v-img
            class="food-image-two"
            src="../assets/products/ayam-taliwang.jpg"
            alt="ayam taliwang"
          />
        </div>
        <div class="image-wrapper-three">
          <!-- Gambar 3 -->
          <v-img
            class="food-image-three"
            src="../assets/products/ayam-kuning.jpg"
            alt="ayam kuning"
          />
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style scoped>
/* GENERAL STYLES */
.hero {
  background-color: #f9f9f9;
  position: relative;
  height: 90vh;
  padding: 0 120px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.text-content {
  max-width: 100%;
  margin-top: -70px;
  padding: 20px 30px;
}

.text-content h1 {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 1.3rem;
  color: #333;
  line-height: 1.2;
}

.text-content span {
  color: #ff4500;
  font-size: 3rem;
  font-weight: bold;
}

.text-content p {
  font-size: 1rem;
  line-height: 1.6;
  color: #555;
  margin-bottom: 2rem;
  text-align: justify;
}

.cta-button {
  background-color: #ff4500;
  color: white;
  border-radius: 5px;
  font-size: 1.1rem;
}

.food-image-one,
.food-image-two,
.food-image-three {
  border-radius: 20px;
  max-width: 100%;
}

.food-image-one {
  width: 135px;
}

.food-image-two {
  width: 180px;
}

.food-image-three {
  width: 340px;
}

.image-content {
  position: relative;
  left: 110px;
  top: -40px;
}

.image-wrapper-one,
.image-wrapper-two {
  position: absolute;
  padding: 7px;
  background-color: #fff;
  border-radius: 20px;
}

.image-wrapper-one {
  bottom: -80px;
  left: 35px;
  z-index: 3;
}

.image-wrapper-two {
  bottom: -17px;
  left: -90px;
  z-index: 2;
}

/* RESPONSIVE STYLES */
@media (max-width: 960px) {
  .hero {
    height: 80vh;
    padding: 0 60px;
  }

  .text-content {
    margin-top: 0;
    padding: 10px 20px;
    text-align: center;
  }

  .text-content p {
    text-align: center;
  }

  .image-content {
    display: flex;
    justify-content: center;
    align-items: center;
    position: static;
  }

  .food-image-one,
  .food-image-two,
  .food-image-three {
    width: 200px;
  }

  .image-wrapper-one,
  .image-wrapper-two,
  .image-wrapper-three {
    position: static;
    background-color: #fff;
    border-radius: 20px;
  }
}

@media (max-width: 650px) {
  .hero {
    height: auto;
    padding: 10px;
  }

  .text-content h1 {
    font-size: 1.8rem;
  }

  .text-content span {
    font-size: 1.8rem;
  }

  /* .image-content {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  } */

  .image-wrapper-one,
  .image-wrapper-two,
  .image-wrapper-three {
    flex-direction: column;
    gap: 10px;
  }

  .food-image-one,
  .food-image-two,
  .food-image-three {
    width: 100px;
  }
}
</style>
