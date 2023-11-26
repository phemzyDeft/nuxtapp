<template>
  <h2>Prodcut page</h2>
  <section>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products">
        <Productcard :product="product" :key="product.id"/>
      </div>
    </div>
  </section>
</template>

<script setup>
  definePageMeta({
    layout: "products"
  })

const { data: products } = await useFetch("https://fakestoreapi.com/products")
// console.log("my product", products)

</script>



