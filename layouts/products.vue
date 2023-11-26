<template>
  <header class="bg-white shadow-sm">
    <nav class="container mx-auto p-4 flex justify-between align-center">
      <NuxtLink to="/products" class="font-bold">Products</NuxtLink>
    </nav>
  </header>

  <div class="container mx-auto p-4">
    <slot></slot>
  </div>
  <div class="text-center">
    <NuxtLink to="/">Back to home page</NuxtLink>
  </div>
</template>

<style>
</style>

