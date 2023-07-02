<template>
  <header class="flex justify-center w-full py-2 px-4 lg:py-5 lg:px-6 bg-yellow-950 bg-border-b border-neutral-200">
    <div class="flex flex-wrap lg:flex-nowrap items-center flex-row justify-start h-full max-w-[1536px] w-full">
      <a href="#" aria-label="SF Homepage"
        class="inline-block mr-4 focus-visible:outline focus-visible:outline-offset focus-visible:rounded-sm shrink-0">
        <img src="~assets/images/nav.png" class="overflow-hidden object-cover h-8 w-80" alt="">
      </a>
      <div class="ms-auto text-white">
        <NuxtLink class="me-5 hover:bg-red-700 py-3 px-5 rounded-lg" to="/">Home </NuxtLink>
        <NuxtLink class="me-5 hover:bg-red-700 py-3 px-5 rounded-lg" to="/about">About </NuxtLink>
        <NuxtLink class="me-5 hover:bg-red-700 py-3 px-5 rounded-lg" to="/products">Products</NuxtLink>
        <NuxtLink class="me-5 hover:bg-red-700 py-3 px-5 rounded-lg" to="/products/byname">Contact</NuxtLink>
        <NuxtLink class="me-5 bg-blue-800 hover:bg-blue-900 py-3 px-5 rounded-lg" to="/products/byname">
          <SfIconSearch />Search
        </NuxtLink>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  import {
    SfButton,
    SfInput,
    SfIconSearch,
    SfIconMenu,
  } from '@storefront-ui/vue';
</script>


<style  scoped>

</style>