<template>
    <div id="formations">
        <h3 class="text-4xl font-thin italic mb-4">Formations</h3>
        <ul class="flex flex-col gap-6 border-l-2 border-gray-200 dark:border-gray-700">   
            <li v-for="(formation, i) in formations" :key="i" class="flex">
                <div class="ml-4 mr-2 w-20 h-20 bg-gray-200 dark:bg-gray-700 rounded-md border-2 border-gray-300 dark:border-gray-600">
                    <img :src="formation.image" alt="Logo" class="w-full h-full object-cover rounded-md">
                </div>
                <div>
                    <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">{{ formation.dates }}</time>
                    <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{{ formation.name }}</h3>
                    <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">{{ formation.description }}</p>
                </div>
            </li>               
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import formationsData from '../assets/json/formations.json';

let formations = ref(formationsData);
</script>