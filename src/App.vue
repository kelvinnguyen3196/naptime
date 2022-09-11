<script setup>
import TheTitle from '@/components/TheTitle.vue';
import InputProjectName from '@/components/InputProjectName.vue';
</script>

<template>
	<div id="page-content">
		<div class="title">
			<TheTitle />
		</div>
		<InputProjectName />
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
	font-size: 3.2rem;
}

h2 {
	color: var(--color-accent);
	font-size: 2.4rem;
}

input[type="text"] {
	color: var(--color-dark);
	font-size: 1.6rem;
}
</style>

<!-- component specific styling -->
<style scoped>
#page-content {
	display: flex;
	flex-direction: column;
	gap: 2rem;
	width: 90vw;
	margin: auto;
}
</style>