<template>
    <div class="gap-5 py-5 bg-yellow-900 text-white">
       <section v-if="pending">
        <img src="~assets/images/loading.png" alt="">
       </section>
       <section v-else>
        <div class=" container m-auto grid grid-cols-6">
            <div class=" col-span-2">
                <h1 class="text-2xl font-semibold py-3 font-serif ">{{meal.meals[0].strMeal}}</h1>
                <img :src="meal.meals[0].strMealThumb" class="rounded-lg" alt="">
            </div>
                <div class=" col-span-2 text-center text-white">
                    <h1 class="text-2xl font-serif hover:text-orange-900 font-semibold py-3">Ingredients</h1>
                    <ol>
                        <li class="py-1">{{meal.meals[0].strIngredient1}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient2}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient3}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient4}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient5}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient6}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient7}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient8}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient9}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient10}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient11}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient12}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient13}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient14}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient15}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient16}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient17}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient18}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient19}}</li>
                        <li class="py-1">{{meal.meals[0].strIngredient20}}</li>
                    </ol>
                </div>
                <div class="col-span-2 text-center text-white">
                    <h1 class="text-2xl font-serif hover:text-orange-900 font-semibold py-3">Measure</h1>
                    <ul>
                        <li class="py-1">{{meal.meals[0].strMeasure1}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure2}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure3}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure4}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure5}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure6}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure7}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure8}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure9}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure10}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure11}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure12}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure13}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure14}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure15}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure16}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure17}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure18}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure19}}</li>
                        <li class="py-1">{{meal.meals[0].strMeasure20}}</li>
                    </ul>
                </div>
                <div class="col-span-6 row-span-2 text-center">
                    <a :href="meal.meals[0].strYoutube" target="_blank" class="font-serif">How to make: <button
                            class="bg-red-600 py-1 px-3 rounded font-serif">Click here</button>
                    </a>
                    </div>
        </div>
        <div class=" py-3 px-3 rounded-md">
            <h1 class="text-4xl font-bold font-serif">#Category:{{meal.meals[0].strCategory}}</h1>
            <h3 class="text-lg font-medium font-mono">ID No: {{ route.params.id}}</h3>
            <p class=" py-3"><span class="font-bold">-Instruction:</span>
                {{meal.meals[0].strInstructions}}</p>
           
        </div>

       </section>
    </div>
</template>

<script setup>
    const route = useRoute();
    const { data: meal } = await useFetch(`https://themealdb.com/api/json/v1/1/lookup.php?i=${route.params.id}`);

    const url = ref(`https://themealdb.com/api/json/v1/1/lookup.php?i=52772`);
    const { data, pending } = await useFetch(url, { refetch: true });


</script>

<style lang="scss" scoped>

</style>