<template>
  <div class="bg-yellow-900">
    <section v-if="pending" >
      <img src="~assets/images/loading.gif" alt="">
    </section>
   <section v-else class="container m-auto">
    <section>
      <div class="lg:grid grid-cols-10 py-6">
        <div class="col-span-2">
          <img src="~assets/images/logo.png" alt="">
        </div>
        <div class="col-span-6 text-center text-white">
          <h1 class="text-5xl font-bold font-serif py-3">Welcome to The Nepalese Kitchen</h1>
          <p>Welcome to The Nepalese Kitchen: An open, crowd-sourced database of Recipes from around the world.<br>
            We also offer a free JSON API for anyone wanting to use it, with additional features for subscribers.</p>
          <button class="bg-amber-600 hover:bg-amber-700 hover:shadow-xl py-2 px-4 rounded text-black my-2">PayPal
            Subscribe</button>
          <p>Click above button to upgrade API for $3 per month (cancel anytime) <br>
            Currently 76 supporters</p>
        </div>
        <div class="col-span-2">
          <img src="~assets/images/logo.png" alt="">
        </div>
      </div>
    </section>
    <hr>
    <section class="py-5 container m-auto">
      <h1 class="text-4xl m-3 text-white font-serif text-center">List Of All Category</h1>
      <div class="container m-auto grid grid-cols-4 gap-5 py-5">
        <div v-for="(c, index) in cate.categories" :key="index">
          <NuxtLink :to="`/categories/${c.idCategory}`">
            <CategoryCard :category="c" />
          </NuxtLink>
        </div>
      </div>
    </section>
   </section>

  </div>
</template>

<script setup>
  const url = ref(`https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood`);

 

  const { data: cate } = await useFetch("https://www.themealdb.com/api/json/v1/1/categories.php");

  const { data,pending } = await useFetch(url, { refetch: true });


</script>

<style lang="scss" scoped>

</style>