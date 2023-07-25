<script setup>
import { ref } from 'vue';

const color = "Color Combination";
const colorLogic = ref("green");
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Color Change Logic</h1>
    <div class="w-800px bg-sky-100 p-10 flex items-center flex-col space-y-10">
      <h1 class="text-3xl">{{ color }}</h1>

      <template v-if="'red' === colorLogic">
        <h2 class="text-2xl">Color: Red</h2>
        <h2 class="text-xl">Hexa Code: #FCA5A5</h2>
        <div class="bg-red-300 p-10 rounded-full text-white"></div>
      </template>

      <template v-if="'blue' === colorLogic">
        <h2 class="text-2xl">Color: blue</h2>
        <h2 class="text-xl">Hexa Code: #93C5FD</h2>
        <div class="bg-blue-300 p-10 rounded-full text-white"></div>
      </template>

      <template v-if="'green' === colorLogic">
        <h2 class="text-2xl">Color: Green</h2>
        <h2 class="text-xl">Hexa Code: #86EFAC</h2>
        <div class="bg-green-300 p-10 rounded-full text-white"></div>
      </template>

      <template v-if="'orange' === colorLogic">
        <h2 class="text-2xl">Color: Orange</h2>
        <h2 class="text-xl">Hexa Code: #FDBA74</h2>
        <div class="bg-orange-300 p-10 rounded-full text-white"></div>
      </template>

      <template v-if="'yellow' === colorLogic">
        <h2 class="text-2xl">Color: Yellow</h2>
        <h2 class="text-xl">Hexa Code: #FDE047</h2>
        <div class="bg-yellow-300 p-10 rounded-full text-white"></div>
      </template>

      <input
        placeholder="Write Your Color"
        class="text-center px-5 p-3"
        type="text"
        v-model="colorLogic"
      />

      <p>Colors Available: [red, green, blue, orange, yellow]</p>
    </div>
  </section>
</template>

<style scoped></style>
