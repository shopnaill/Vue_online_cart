<template>
  <div class="home">
    <div class="container">
      <ProductsPage />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductsPage from "@/components/ProductsPage.vue";

export default {
  name: "home",

  components: {
    ProductsPage
  }
};
</script>
