<template>
  <h2>{{ error.statusCode }}</h2>
  <p>Ooops...</p>
  <h2>{{ error.message }}</h2>

  <button class="btn" @click="handleRedirect">Continue shopping</button>
</template>

<script setup>
defineProps(["error"])

const handleRedirect = () => clearError({redirect: "/products", fatal: true})
</script>