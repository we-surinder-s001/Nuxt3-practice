<script setup>
useHead({
  title: "App Product page",
});
definePageMeta({
  layout: "products-layout",
});
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<template>
  <div>
    <h1 class="pb-20">Products:</h1>
    <div class="grid grid-cols-4 gap-7">
      <div v-for="product in products" :key="product.id">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>
