<template>
  <div class="card">
    <div class="grid grid-cols-2 gap-10">
      <img :src="product.image" :alt="product.title" class="mx-auto my-7" />
      <div class="p-7">
        <h2 class="text-4xl my-7">{{ product.title }}</h2>
        <p class="text-xl my-7">${{ product.price }}</p>
        <h3 class="font-bold border-b-2 mb-2 pb-2">Product Description:</h3>
        <p class="mb-7">{{ product.description }}</p>
        <button class="btn flex">
          <i class="material-icons mr-2">add_shopping_cart</i>
          <span>Add to Cart</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"])
</script>

<style scoped>
  img{
    max-width: 300px;
  }
</style>