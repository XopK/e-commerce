<script setup>
</script>

<template>
    <section class="hero w-full px-4 py-8 sm:px-8 sm:py-12 lg:px-25 lg:py-25">
        <div class="hero-text text-center w-full max-w-xs sm:max-w-lg lg:max-w-2xl mx-auto">
            <h2 class="uppercase font-integral font-bold text-2xl sm:text-4xl lg:text-6xl leading-tight">
                Find clothes that matches your style
            </h2>

            <p class="font-satoshi font-normal opacity-60 mt-4 sm:mt-6 lg:mt-8 text-sm sm:text-base">
                Browse through our diverse range of meticulously crafted
                garments, designed to bring
                out your individuality and cater to your sense of style.
            </p>

            <button class="btn btn-primary mt-4 sm:mt-6 lg:mt-8 font-satoshi font-medium px-6 py-3 sm:px-8 sm:py-4">
                Shop Now
            </button>

            <div class="more-hero-text mt-6 sm:mt-8 lg:mt-10">
                <ul class="flex flex-col sm:flex-row justify-center font-satoshi gap-4 sm:gap-0">
                    <li class="text-center sm:pr-4 lg:pr-8">
                        <div class="text-2xl sm:text-3xl lg:text-4xl font-bold">200+</div>
                        <span class="text-xs sm:text-sm lg:text-base font-normal opacity-60">International Brands</span>
                    </li>
                    <li class="text-center sm:border-l-2 border-gray-300 sm:px-4 lg:px-8">
                        <div class="text-2xl sm:text-3xl lg:text-4xl font-bold">2,000+</div>
                        <span class="text-xs sm:text-sm lg:text-base font-normal opacity-60">High-Quality
                            Products</span>
                    </li>
                    <li class="text-center sm:border-l-2 border-gray-300 sm:pl-4 lg:pl-8">
                        <div class="text-2xl sm:text-3xl lg:text-4xl font-bold">30,000+</div>
                        <span class="text-xs sm:text-sm lg:text-base font-normal opacity-60">Happy Customers</span>
                    </li>
                </ul>
            </div>
        </div>
    </section>
    <section class="brand-tape w-full">
        <div class="flex items-center justify-center py-11  gap-26">
            <img src="@/assets/images/Versace.png" alt="Verace">
            <img src="@/assets/images/Zara.png" alt="Zara">
            <img src="@/assets/images/Gucci.png" alt="Gucci">
            <img src="@/assets/images/Prada.png" alt="Prada">
            <img src="@/assets/images/Calvin.png" alt="Calvin Klein">
        </div>
    </section>
    <section class="new-arrivals w-full mt-18">
        <h3 class="font-integral text-center font-bold text-5xl">New arrivals</h3>
    </section>
</template>

<style scoped>
.hero {
    background-color: #F2F0F1;
}
.brand-tape{
    background-color: #000000;
}
</style>