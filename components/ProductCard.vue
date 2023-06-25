<template>
  <div class=" rounded-md w-200px h-100px">
    <div class="relative">
      <SfLink href="#">
        <img :src="product.strMealThumb" alt="Great product" class="block object-cover h-auto rounded-md border-y-2  border-yellow-950  aspect-square hover:shadow-xl"
          :width="300" :height="300" />
      </SfLink>
    </div>
    <div class="p-4 text-base text-white text-center font-serif">
      <SfLink href="#" variant="secondary" class="no-underline"> {{product.strMeal}} </SfLink>
    </div>
  </div>
</template>

<script lang="ts" setup>
  import { SfRating, SfCounter, SfLink, SfButton, SfIconShoppingCart, SfIconFavorite } from '@storefront-ui/vue';
  defineProps({
    product: {},
  })
</script>