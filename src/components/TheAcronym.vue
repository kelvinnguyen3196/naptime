<script setup>
// imports
import CopiedBanner from '@/components/CopiedBanner.vue';
import { useCopiedBannerStore } from '@/stores/copiedBanner.js';
import { useAcronymStore } from '@/stores/acronym.js';
import { ref } from 'vue';

// use imports
const acronym = useAcronymStore();
const copiedBanner = useCopiedBannerStore();

// template refs
const copiedBannerElem = ref(null);

// copy button
const copyButton = ref(null);
const copyToClipboard = () => {
    // active copied banner for two seconds
    copiedBanner.active = true;
    setTimeout(() => {
        copiedBanner.active = false;
    }, 2000);
    
    if(!acronym.initals) {
        navigator.clipboard.writeText(``);
        return;
    }
    navigator.clipboard.writeText(acronym.initals);
    
}
</script>

<template>
    <div class="container">
        <h2>your project acronym - <span>{{ acronym.initals }}</span></h2>
        <img @click="copyToClipboard" ref="copyButton" src="@/assets/copy.svg" alt="copy icon">
        <CopiedBanner />
    </div>
</template>

<style scoped>
span {
    color: var(--color-light);
}

.container {
    display: flex;
    gap: 1rem;
    align-items: center;
}

img {
    height: 2.4rem;
    aspect-ratio: 1;
    cursor: pointer;
}

img:active {
    filter: brightness(0.5);
}
</style>