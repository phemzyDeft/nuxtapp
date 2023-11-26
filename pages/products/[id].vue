<template>
  <div>

    <Head>
      <Title>E-Commerce | {{ product_details.title }}</Title>
      <Meta name="description" :content="product_details.description"/>
    </Head>

    <Productdetails :product="product_details" :key="product_details.id"/>
  </div>  
</template>

<script setup>

definePageMeta({
  layout: "products",
})

const { id } = useRoute().params

const url = "https://fakestoreapi.com/products/" + id

const { data: product_details } = await useFetch(url, { key: id })
if (!product_details.value) {
  throw createError({statusCode: 404, statusMessage: "page not found"})
}
// console.log("fake store api", product)

</script>