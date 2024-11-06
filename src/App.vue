
<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => {
    if (count.value < 10) {
      count.value++
    }

}
const decrement = () => {
 if (count.value > 0) {
      count.value--
    }
}
</script>

<template>
  <div class="min-h-screen flex flex-col justify-center items-center bg-gray-200">
     <h1 class="text-4xl font-bold text-gray-800">Counter</h1>
      <div class="flex gap-2 justify-center items-center p-4">
        <button @click="decrement()" class="border-2 border-gray-600 bg-gray-200 p-2 rounded-lg">Decrement</button>
        <p class="text-4xl font-bold text-gray-800 p-2 h-20 w-20 text-center flex justify-center items-center bg-amber-500 rounded-lg">{{ count }}</p>
        <button @click="increment()" class="border-2 border-gray-600 bg-gray-200 p-2 rounded-lg">Increment</button>
      </div>

  </div>
</template>


<style lang="scss" scoped>

</style>