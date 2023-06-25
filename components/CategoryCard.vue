<template>
  <div class=" rounded-md w-200px h-100px">
    <div class="relative">
      <SfLink href="#">
        <img :src="category.strCategoryThumb" alt="Great product" class="block object-cover border-y-2  border-yellow-950 h-auto rounded-md aspect-square hover:shadow-xl"
          :width="300" :height="300" />
      </SfLink>
    </div>
    <div class="p-4 text-base text-center  text-white ">
      <SfLink href="#" variant="secondary" class="no-underline text-lg font-medium"> {{category.strCategory}} </SfLink>
      <p class="line-clamp-3 font-serif">{{category.strCategoryDescription}}</p>
    </div>
  </div>
</template>
<script lang="ts" setup>
  import { SfRating, SfCounter, SfLink, SfButton, SfIconShoppingCart, SfIconFavorite } from '@storefront-ui/vue';
  defineProps({
    category: {},
  })
</script>