<script setup>
import TheTitle from '@/components/TheTitle.vue';
import TheAcronym from '@/components/TheAcronym.vue';
import InputProjectName from '@/components/InputProjectName.vue';
</script>

<template>
	<div id="page-content">
		<div class="title-container">
			<TheTitle />
		</div>
		<div class="acronym-container">
			<TheAcronym />
			<InputProjectName />
		</div>
	</div>
</template>

<!-- general styling -->
<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;700&display=swap');
:root {
	--color-dark: #222831;
	--color-mid: #393E46;
	--color-light: #EEEEEE;
	--color-accent: #00ADB5;

	--transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.5s;

	font-size: 62.5%;	/* base font size for most 10px now */
}

* {
	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

body {
	background: var(--color-dark);
	font-family: 'Poppins', sans-serif;
	color: var(--color-light);
}

h1 {
	font-size: 4rem;
}

h2 {
	color: var(--color-accent);
	font-size: 2.4rem;
}

input[type="text"], p {
	color: var(--color-dark);
	font-size: 1.6rem;
}
</style>

<!-- component specific styling -->
<style scoped>
#page-content {
	display: flex;
	flex-direction: column;
	gap: 3rem;
	width: min(80%, 800px);
	margin: auto;
	margin-block: 2rem;
}

.acronym-container {
	width: 100%;
	display: flex;
	flex-direction: column;
	gap: 1rem;
}
</style>