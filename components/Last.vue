<template>
    <div class="w-full h-250px bg-yellow-950 py-5">
        <div class="grid grid-cols-12 container m-auto text-white">
            <div class="col-span-4 flex text-center">
                <img src="~assets/images/logo.png" class="overflow-hidden object-cover h-38 w-60" alt="">
            </div>
            <div class="col-span-2 py-2">
                    <ol>
                        <li>
                            <NuxtLink to="/">Home </NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/about">About </NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/products">Products</NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/products/byname">Contact</NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/products/byname">
                                <SfIconSearch />Search
                            </NuxtLink>
                        </li>
                    </ol>
            </div>
            <div class="col-span-2 text-center py-2">
                <h1 class="text-lg">We Accept</h1>
                <ol>
                    <li><a href="">Esewa</a></li>
                    <li><a href="">Khalti</a></li>
                    <li><a href="">Mobile Banking</a></li>
                    <li><a href="">QR Code</a></li>
                </ol>
            </div>
            <div class="col-span-4 text-center py-5">
                <h1 class="text-lg">2023 The Nepalese Kitchen<br>
                    Proudly built by Anjila_Tg</h1>
            </div>

        </div>
    </div>

</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>