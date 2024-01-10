<script setup>
definePageMeta({
  layout: "products-layout"
})
const {id} = useRoute().params;

const uri = `https://fakestoreapi.com/products/${id}`;

const {data: product} = await useFetch(uri, {key: id});


</script>

<template>
  <div>
    <img :src="product.image" :alt="product.title">
    <br>
    <h2>{{ product.title }}</h2>
    <br>
    <p>description : {{ product.description }}</p>
    <br>
    <p>Price : {{ product.price }}</p>
  </div>
</template>