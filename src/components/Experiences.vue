<template>
    <div id="experiences-pro">
        <h3 class="text-4xl font-thin italic mb-4">Expériences professionnelles</h3>
        <ol class="relative border-s border-gray-200 dark:border-gray-700">                  
            <li v-for="(experience, i) in experiences" :key="i" class="mb-10 ms-4">
                <span v-if="experience.inProgress" class="bg-purple-100 text-purple-800 text-xs font-medium me-2 px-2.5 py-0.5 rounded dark:bg-purple-900 dark:text-purple-300">En cours</span>
                <span v-else class="bg-green-100 text-green-800 text-xs font-medium me-2 px-2.5 py-0.5 rounded dark:bg-green-900 dark:text-green-300">Terminée</span>
                <div class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -start-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"></div>
                <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">{{experience.start}} - {{experience.end}}</time>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{{experience.name}}</h3>
                <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">{{ experience.extract }}</p>
                <button @click="selectExperience(experience)" type="button" data-modal-target="exp" data-modal-toggle="exp" class="inline-flex items-center px-4 py-2 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:outline-none focus:ring-gray-100 focus:text-blue-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700 dark:focus:ring-gray-700">En savoir plus <svg class="w-3 h-3 ms-2 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                    </svg>
                </button>
            </li>
        </ol>

        <Modal :exp="experienceSelected" />
    </div>
    <div id="experiences-asso" class="mt-6">
        <h3 class="text-4xl font-thin italic mb-4">Expériences associatives</h3>
        <ol class="relative border-s border-gray-200 dark:border-gray-700">                  
            <li v-for="(experience, i) in experiencesAsso" :key="i" class="mb-10 ms-4">
                <span v-if="experience.inProgress" class="bg-purple-100 text-purple-800 text-xs font-medium me-2 px-2.5 py-0.5 rounded dark:bg-purple-900 dark:text-purple-300">En cours</span>
                <span v-else class="bg-green-100 text-green-800 text-xs font-medium me-2 px-2.5 py-0.5 rounded dark:bg-green-900 dark:text-green-300">Terminée</span>
                <div class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -start-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"></div>
                <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500">{{experience.start}} - {{experience.end}}</time>
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white">{{experience.name}}</h3>
                <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">{{ experience.extract }}</p>
                <button @click="selectExperience(experience)" type="button" data-modal-target="exp" data-modal-toggle="exp" class="inline-flex items-center px-4 py-2 text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:outline-none focus:ring-gray-100 focus:text-blue-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700 dark:focus:ring-gray-700">En savoir plus <svg class="w-3 h-3 ms-2 rtl:rotate-180" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                    </svg>
                </button>
            </li>
        </ol>

        <Modal :exp="experienceSelected" />
    </div>
</template>

<script setup>
import { ref } from 'vue';
import experiencesData from '../assets/json/experiences.json';
import experiencesAssoData from '../assets/json/experiences_asso.json';
import Modal from './Modal.vue';

let experienceSelected = ref('');

const selectExperience = (experience) => {
    experienceSelected.value = experience;
}

let experiences = ref(experiencesData);
let experiencesAsso = ref(experiencesAssoData);
</script>