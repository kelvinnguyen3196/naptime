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
    acronym.initals = initals;
}
</script>

<template>
    <input @input="formatData" v-model="acronym.rawData" type="text">
</template>

<style>
input[type="text"] {
    all: unset;
    background: var(--color-light);
    padding: 0.5rem;
    border-radius: 0.5rem;
}
</style>