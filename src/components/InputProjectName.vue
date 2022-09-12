<script setup>
// imports
import { useAcronymStore } from '@/stores/acronym.js';

// use imports
const acronym = useAcronymStore();

// format acronym
const formatData = () => {
    const words = acronym.rawData.split(` `);
    let initals = ``;
    words.forEach((word) => {
        // append first letter of word
        initals = initals.concat(word.charAt(0));
    });
    acronym.initals = initals.toLowerCase();
}
</script>

<template>
    <input @input="formatData" v-model="acronym.rawData" type="text" placeholder="type project name...">
</template>

<style>
input[type="text"] {
    all: unset;
    background: var(--color-light);
    padding-block: 0.5rem;
    padding-inline: 0.8rem;
    border-radius: 0.5rem;
    width: 100%;
}
</style>