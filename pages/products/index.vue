<script setup>
definePageMeta({
  layout: "products-layout"
})

const {data: products} = await useFetch('https://fakestoreapi.com/products')

</script>

<template>
  <div>
    <h1 class="pb-20">Products: </h1>
    <div class="grid grid-cols-4 gap-7">
      <Nuxt-link v-for="product in products" :key="product.id" :to="`/products/${product.id}`">
        <div class="shadow-md p-10">
          <img :src="product.image" :alt="product.title">
          <h3 class="mt-4">{{ product.title }}</h3>
        </div>
      </Nuxt-link>
    </div>
  </div>
</template>
