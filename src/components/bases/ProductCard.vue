<script setup>
import { computed } from 'vue';
import StarRating from '../utilities/StarRating.vue';

const props = defineProps({
    image: { type: String, required: true },
    title: { type: String, required: true },
    rating: { type: Number, required: true },
    price: { type: Number, required: true },
    oldPrice: { type: Number, required: false }
})

const discount = computed(() => {
    if (!props.oldPrice || props.oldPrice <= props.price) return null
    return Math.round(((props.oldPrice - props.price) / props.oldPrice) * 100)
})
</script>

<template>
    <div class="card">
        <img class="rounded-3xl transition-transform duration-200 ease-in-out hover:scale-[1.03] cursor-pointer" :src="image" :alt="title">
        <h4 class="font-satoshi font-bold text-xl mb-2 mt-4">{{ title }}</h4>
        <StarRating :rating="rating" />
        <p class="font-satoshi font-bold text-2xl flex items-center mt-2 gap-3">
            <span>${{ price }}</span>
            <span v-if="oldPrice" class="text-gray-400 line-through">
                ${{ oldPrice }}
            </span>
            <span v-if="discount" class="bg-[#FF3333]/20 py-[6px] px-[14px] rounded-full text-xs text-[#FF3333]">
                -{{ discount }}%
            </span>
        </p>
    </div>
</template>