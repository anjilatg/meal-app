<template>
    <div class="bg-yellow-900">
        <section v-if="pending">
           <div class="flex justify-center align-middle">
            <img src="~assets/images/loading.gif" alt="">
           </div>
        </section>
        <section v-else>
            <section>
                <div class="container m-auto py-4">
                    <div>
                        <div class="text-center text-white">
                            <label for="" class=" text-center form-label font-serif text-lg bg">Select category</label>
                        </div>
                        <div>
                            <select
                                class="form-select form-select-lg w-full text-center h-10 rounded font-serif hover:shadow-xl  bg-yellow-950 text-white"
                                v-model="name" @change="getUrl(name)">
                                <option selected>Select One</option>
                                <option :value="category.strCategory" v-for="(category,index) in categoryDAta.categories"
                                    :key="index">
                                    {{category.strCategory}}</option>
                            </select>
                        </div>
                    </div>
                </div>
            </section>
            <section>
                <div class="container m-auto grid lg:grid-cols-4  md:grid-cols-2 gap-5 py-3">
                    <div v-for="(p, index) in data.meals" :key="index">
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
    let name = "Select One";
    const url = ref(`https://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood`);

    const { data: categoryDAta } = await useFetch("https://www.themealdb.com/api/json/v1/1/categories.php");
    const { data, pending } = await useFetch(url, { refetch: true });

    function getUrl(category) {
        url.value = `https://www.themealdb.com/api/json/v1/1/filter.php?c=${category}`
    };
</script>

<style lang="scss" scoped>

</style>