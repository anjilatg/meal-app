<template>
    <div class="w-full h-250px bg-yellow-950 py-5">
        <div class="grid grid-cols-15 container m-auto text-white">
            <div class="col-span-6 flex text-center">
                <img src="~assets/images/logo.png" class="overflow-hidden object-cover h-38 w-60" alt="">
            </div>
            <div class="col-span-3">
                <div class="ms-auto text-white">
                    <ol>
                        <li>
                            <NuxtLink to="/">Home </NuxtLink>
                            <NuxtLink to="/about">About </NuxtLink>
                            <NuxtLink to="/products">Products</NuxtLink>
                            <NuxtLink to="/products/byname">Contact</NuxtLink>
                            <NuxtLink to="/products/byname">
                                <SfIconSearch />Search
                            </NuxtLink>
                        </li>
                    </ol>
                </div>
            </div>
            <div class="col-span-2 text-center">
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