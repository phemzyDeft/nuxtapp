<template>
  <div>
    <header class="bg-white shadow-sm">
      <nav class="container mx-auto p-4 flex justify-between align-center">
        <NuxtLink to="/" class="font-bold">Shopping</NuxtLink>
        <ul class="flex align-center gap-4">
          <li class="router-link-active">
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li class="router-link-active">
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li class="router-link-active">
            <NuxtLink to="/products" class="btn">Product</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
  </div>

  <div class="container mx-auto p-4">
    <slot></slot>
  </div>
</template>

<style>
.router-link-exact-active {
  color: green;
}
</style>