<template>
    <ul class="flex gap-5 mt-5">
        <li v-for="link in socialLinks" :key="link.name">
            <a :href="link.url" target="_blank">
                <i :class="link.icon + ' text-2xl'"></i>
            </a>
        </li>
    </ul>
</template>

<script setup>
import { defineProps } from 'vue'
defineProps({
    socialLinks: {
        type: Array,
        default: () => [
            {
                name: 'LinkedIn',
                url: 'https://www.linkedin.com/in/alexis-briet',
                icon: 'fa-brands fa-linkedin'
            },
            {
                name: 'GitHub',
                url: 'https://www.github.com/BrietGame',
                icon: 'fa-brands fa-github'
            }
        ]
    }
})
</script>