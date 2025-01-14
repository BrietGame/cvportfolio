<template>
    <div id="realisations">
        <h3 class="text-3xl sm:text-4xl font-thin italic mb-4">Réalisations</h3>
        <div class="flex flex-wrap gap-5">
            <a v-for="(realisation, i) in realisations" :key="i" :href="realisation.link" target="_blank" class="flex flex-col items-center bg-white border border-gray-200 rounded-lg shadow md:flex-row md:max-w-xl hover:bg-gray-100 dark:border-gray-700 dark:bg-gray-800 dark:hover:bg-gray-700">
                <img class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-s-lg" :src="realisation.image" alt="">
                <div class="flex flex-col justify-between p-4 leading-normal">
                    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{{ realisation.name }}</h5>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ realisation.description }}</p>
                </div>
            </a>
        </div>
    </div>
</template>

<script setup>
import realisationsData from '../assets/json/realisations.json';
import { ref } from 'vue';

let realisations = ref(realisationsData);
</script>