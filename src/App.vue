<script setup>
import Bio from './components/Bio.vue';
import SocialLink from './components/SocialLink.vue'
import Summary from './components/Summary.vue'
import Skills from './components/Skills.vue';
import Realisations from './components/Realisations.vue';
import Formations from './components/Formations.vue';
import Experiences from './components/Experiences.vue';


</script>

<template>
  <main>
        <section class="mt-10">
            <div class="flex gap-10 w-full justify-between">
                <img
                src="./assets/alexis.jpg"
                alt=""
                class="size-80 rounded-lg object-cover"
                />
                <div class="self-end flex flex-col gap-5">
                    <p class="text-2xl font-thin italic text-gray-900">Disponible pour un poste de</p>
                    <h1 class="text-5xl font-bold text-gray-900">Développeur web / web mobile</h1>
                </div>
                <div class="self-start flex flex-col gap-5 pt-10">
                    <span class="text-1xl font-bold"><i class="fa-solid fa-location-arrow text-2xl"></i> 76000 Rouen</span>
                    <span class="text-1xl font-bold"><i class="fa-solid fa-magnifying-glass text-2xl"></i> CDI - CDD - Freelance</span>
                </div>
            </div>
            
            <h2 class="mt-6 text-6xl font-bold text-gray-900">Alexis</h2>
            <h2 class="text-4xl font-bold text-gray-900">BRIET</h2>
            <SocialLink />
        </section>
        <section class="flex gap-4 mt-10 w-full">
            <Summary />

            <div class="w-3/4 flex flex-col gap-20">
                <Bio />

                <Skills />

                <Experiences />

                <Formations />

                <Realisations />
            </div>
        </section>
        <div id="alert-additional-content-1" class="fixed bottom-0 left-5 p-4 mb-4 text-blue-800 border border-blue-300 rounded-lg bg-blue-50 dark:bg-gray-800 dark:text-blue-400 dark:border-blue-800" role="alert">
            <div class="flex items-center">
                <svg class="flex-shrink-0 w-4 h-4 me-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
                <path d="M10 .5a9.5 9.5 0 1 0 9.5 9.5A9.51 9.51 0 0 0 10 .5ZM9.5 4a1.5 1.5 0 1 1 0 3 1.5 1.5 0 0 1 0-3ZM12 15H8a1 1 0 0 1 0-2h1v-3H8a1 1 0 0 1 0-2h2a1 1 0 0 1 1 1v4h1a1 1 0 0 1 0 2Z"/>
                </svg>
                <span class="sr-only">Info</span>
                <h3 class="text-lg font-medium">Code GitHub</h3>
            </div>
            <div class="mt-2 mb-4 text-sm">
                Retrouvez le code de ce cv portfolio sur mon GitHub.
            </div>
            <div class="flex">
                <a href="https://github.com/BrietGame/cvportfolio" target="_blank" class="text-white bg-blue-800 hover:bg-blue-900 focus:ring-4 focus:outline-none focus:ring-blue-200 font-medium rounded-lg text-xs px-3 py-1.5 me-2 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                    <svg class="me-2 h-3 w-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 14">
                        <path d="M10 0C4.612 0 0 5.336 0 7c0 1.742 3.546 7 10 7 6.454 0 10-5.258 10-7 0-1.664-4.612-7-10-7Zm0 10a3 3 0 1 1 0-6 3 3 0 0 1 0 6Z"/>
                    </svg>
                    Voir le repo GitHub
                </a>
                <button type="button" class="text-blue-800 bg-transparent border border-blue-800 hover:bg-blue-900 hover:text-white focus:ring-4 focus:outline-none focus:ring-blue-200 font-medium rounded-lg text-xs px-3 py-1.5 text-center dark:hover:bg-blue-600 dark:border-blue-600 dark:text-blue-400 dark:hover:text-white dark:focus:ring-blue-800" data-dismiss-target="#alert-additional-content-1" aria-label="Close">
                    Fermer
                </button>
            </div>
        </div>
    </main>
</template>