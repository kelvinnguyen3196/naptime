<script setup>
import TheTitle from '@/components/TheTitle.vue';
</script>

<template>
	<TheTitle />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;700&display=swap');
:root {
	--color-dark: #222831;
	--color-mid: #393E46;
	--color-light: #EEEEEE;
	--color-accent: #00ADB5;
}

* {
	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

body {
	background: var(--color-dark);
	font-family: 'Poppins', sans-serif;
}

h1 {
	color: var(--color-light);
}

h2 {
	color: var(--color-accent);
}
</style>