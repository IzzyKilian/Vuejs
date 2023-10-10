<template>
  <div>
    <v-row>
      <v-col cols="3" sm="3" v-for="(feature, i) in featured" :key="i">
        <v-card class="mx-auto my-12 pb-4" max-width="374">
          <!-- Tampilkan informasi produk fitur di sini -->
          <v-img height="250" class="mx-4" :src="feature.img"></v-img>
          <v-card-item class="mt-n4">
            <v-card-title class="text-center">{{ feature.title }}</v-card-title>
          </v-card-item>
          <v-card-text>
            <div class="text-center">{{ feature.bio }}</div>
            <v-row align="center" class="mx-0 mt-2">
              <v-rating
                :model-value="4.5"
                color="amber"
                density="compact"
                half-increments
                readonly
                size="small"
              ></v-rating>
              <v-spacer></v-spacer>
              <div class="text-grey ms-4">{{ feature.price }}</div>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  

    <v-row>
      <v-col v-for="product in filteredProducts" :key="product.id" cols="12" sm="6" md="4" lg="3">
        <v-card>
          <v-card-title>{{ product.name }}</v-card-title>
          <v-card-text>{{ product.description }}</v-card-text>
          <v-card-actions>
            <v-btn color="primary" @click="addToCart(product)">Beli</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    featured: [
      {
        img: "image/5.png",
        title: "Smart Tv",
        price: "$ 12.435",
        bio: " Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.",
      },
      {
        img: "image/6.png",
        title: "Airpods",
        price: "$ 5.555",
        bio: " Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.",
      },
      {
        img: "image/7.png",
        title: "Play Station 3",
        price: "$ 9.999",
        bio: " Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.",
      },
      {
        img: "image/8.png",
        title: "Printer",
        price: "$ 23.435",
        bio: " Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.",
      },
    ],
  }),
  props: {
    filteredProducts: Array, // Anda menerima filteredProducts sebagai properti dari komponen induk.
  },
  methods: {
    addToCart(product) {
      // Tambahkan logika untuk menambahkan produk ke dalam keranjang di sini.
      // Anda dapat mengirimkan produk yang dipilih ke komponen induk
      // dengan memancarkan sebuah event atau menggunakan store jika Anda menggunakan Vuex.
    },
  },
};
</script>

<style></style>
