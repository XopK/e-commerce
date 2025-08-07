<script setup>
import { computed } from 'vue'

const props = defineProps({
  rating: {
    type: Number,
    required: true
  }
})

const stars = computed(() => {
  const arr = []
  for (let i = 1; i <= 5; i++) {
    if (props.rating >= i) {
      arr.push('full')
    } else if (props.rating >= i - 0.5) {
      arr.push('half')
    } else {
      arr.push('empty')
    }
  }
  return arr
})
</script>

<template>
  <div class="flex items-center">
    <template v-for="(type, index) in stars" :key="index">
      <svg
        v-if="type === 'full'"
        xmlns="http://www.w3.org/2000/svg"
        class="w-5 h-5 fill-yellow-500"
        viewBox="0 0 24 24"
      >
        <path
          d="M12 .587l3.668 7.568 8.332 1.151-6.064 5.769 
             1.516 8.275L12 18.896l-7.452 4.454 
             1.516-8.275L0 9.306l8.332-1.151z"
        />
      </svg>

      <svg
        v-else-if="type === 'half'"
        xmlns="http://www.w3.org/2000/svg"
        class="w-5 h-5"
        viewBox="0 0 24 24"
      >
        <defs>
          <linearGradient :id="'half-star-' + index">
            <stop offset="50%" stop-color="rgb(234 179 8)" />
            <stop offset="50%" stop-color="rgb(209 213 219)" />
          </linearGradient>
        </defs>
        <path
          :fill="'url(#half-star-' + index + ')'"
          d="M12 .587l3.668 7.568 8.332 1.151
             -6.064 5.769 1.516 8.275L12 18.896l-7.452 4.454
             1.516-8.275L0 9.306l8.332-1.151z"
        />
      </svg>

      <svg
        v-else
        xmlns="http://www.w3.org/2000/svg"
        class="w-5 h-5 fill-gray-300"
        viewBox="0 0 24 24"
      >
        <path
          d="M12 .587l3.668 7.568 8.332 1.151-6.064 5.769 
             1.516 8.275L12 18.896l-7.452 4.454 
             1.516-8.275L0 9.306l8.332-1.151z"
        />
      </svg>
    </template>

    <span class="ml-3 text-sm text-gray-600">{{ rating }}/5</span>
  </div>
</template>
