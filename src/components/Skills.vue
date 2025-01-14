<template>
    <div id="skills">
        <h3 class="text-3xl sm:text-4xl font-thin italic mb-4">Compétences</h3>
        <div class="flex flex-wrap gap-5">
            <a v-for="(skill, i) in skills" :key="i" href="#" class="bg-blue-100 hover:bg-blue-200 text-blue-800 text-xs font-semibold me-2 px-2.5 py-0.5 rounded dark:bg-gray-700 dark:text-blue-400 border border-blue-400 inline-flex items-center justify-center">{{ skill.name }}</a>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import skillsJson from '../assets/json/skills.json';

let skills = ref(skillsJson);
</script>