<script setup>
// imports
import { useCopiedBannerStore } from '@/stores/copiedBanner.js';
import { watch } from 'vue';

// use imports
const copiedBanner = useCopiedBannerStore();
</script>

<template>
    <div ref="copiedBannerElem" :class="['copied-banner', copiedBanner.active ? '' : 'hidden']">
        <p>Copied!</p>
    </div>
</template>

<style>
.copied-banner {
    background: black;
    padding-inline: 1rem;
    padding-block: 0.5rem;
    border-radius: 1rem;
}

.copied-banner p {
    color: var(--color-light);
}

.hidden {
    display: none;
}
</style>