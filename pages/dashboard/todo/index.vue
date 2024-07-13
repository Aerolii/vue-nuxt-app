<script setup lang="ts">
definePageMeta({
	layout: "dashboard",
})
</script>

<template>
	<div class="p-3 flex-col">
		<header
			class="uppercase font-serif font-medium text-3xl text-red-300 text-center mb-4">
			Todos
		</header>

		<main>
			<TextInput />
		</main>
	</div>
</template>

<style scoped></style>
