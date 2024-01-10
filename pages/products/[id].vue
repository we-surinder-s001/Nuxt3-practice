<script setup>
definePageMeta({
  layout: "products-layout",
});
const { id } = useRoute().params;

const uri = `https://fakestoreapi.com/products/${id}`;

const { data: product } = await useFetch(uri, { key: id });

if (!product.value) {
  throw createError({
    statusCode: 404,
    message: `Product not found with id: ${id}`,
  });
}
</script>

<template>
  <div>
    <ProductDetails :details="product" />
  </div>
</template>
