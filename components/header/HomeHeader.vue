<script setup lang="ts">
defineOptions({
	inheritAttrs: false,
})
</script>

<template>
	<header class="w-full border-b h-14">
		<div class="mx-auto flex items-center h-full space-x-6" v-bind="$attrs">
			<div class="w-[260px] flex justify-start">
				<HomeLink />
			</div>
			<div class="flex-1">
				<NuxtLink to="/dashboard">Dashboard</NuxtLink>
			</div>
			<div>user</div>
		</div>
	</header>
</template>

<style scoped></style>
