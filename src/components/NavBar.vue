<template>
  <v-app-bar flat>
    <template v-slot:prepend>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title>Shopify</v-app-bar-title>
    <v-spacer></v-spacer>
    <v-text-field
      density="Compact"
      variant="solo"
      label="Search Product"
      append-inner-icon="mdi-magnify"
      single-line
      hide-details
      flat
      v-model="searchTerm"
      @input="searchProducts"
    ></v-text-field>
    <v-btn>Download App</v-btn>
    <v-btn>SIGN IN / LOGIN</v-btn>
  </v-app-bar>

</template>

<script>
export default {
  data() {
    return {
      searchTerm: '',
      products: [ /* Daftar produk Anda */ ],
    };
  },
  computed: {
    filteredProducts() {
      // Logika pencarian produk di sini.
      // Misalnya, jika `products` adalah array produk:
      return this.products.filter(product => {
        return product.name.toLowerCase().includes(this.searchTerm.toLowerCase());
      });
    },
  },
  methods: {
    searchProducts() {
      // Panggil metode ini saat input kolom pencarian berubah.
      // Anda dapat meninggalkan metode ini kosong jika tidak memerlukan logika tambahan di sini.
    },
  },
};
</script>

<style>

</style>
