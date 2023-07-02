<template>
    <div class="bg-yellow-900">
        <section v-if="pending">
            <div class="flex justify-center align-middle">
                <img src="~assets/images/loading.gif" alt="">
                </div>
        </section>
        <section v-else class="py-5 container  m-auto text-white  ">
            <div class="flex text-center gap-2">
                <h1 class="py-2 text-lg">Search:</h1>
                <input v-model="ch" type="text" class=" bg-yellow-950 h-10 w-full px-2 rounded-lg
                hover:shadow-xl [&::-webkit-search-cancel-button]:appearance-none py-2 " />
                <span><button @click="getUrl(ch)" type="submit" to="/products" class="flex py-2 px-2 rounded-lg hover:bg-green-800 shadow-lg bg-green-700"><SfIconSearch />search</button></span>
            </div>
            <section>
                <div class="container m-auto lg:grid grid-cols-4 gap-5 py-3">
                    <div v-for="(p, index) in meal.meals" :key="index">
                        <NuxtLink :to="`/products/${p.idMeal}`">
                            <ProductCard :product="p" />
                        </NuxtLink>
                    </div>
                </div>
            </section>

        </section>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import {
        SfButton,
        SfInput,
        SfIconSearch,
        SfIconMenu,
    } from '@storefront-ui/vue';
    const ch = ref("Arrabiata")

    const url = ref('https://themealdb.com/api/json/v1/1/search.php?s=Arrabiata');
    const { data: meal,pending } = await useFetch(url, { refetch: true });

    function getUrl(ch) {
        url.value = `https://themealdb.com/api/json/v1/1/search.php?s=${ch}`;
    }
</script>

<style lang="scss" scoped>

</style>