<script setup>
definePageMeta({
  layout: "products-layout"
})
const {id} = useRoute().params
</script>

<template>
  <h1>
    {{ id }}
  </h1>
</template>