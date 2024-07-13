<script setup lang="ts">
const navs = [
	{
		name: "dashboard",
		path: "/dashboard",
	},
	{
		name: "todo",
		path: "/dashboard/todo",
	},
]
</script>

<template>
	<div class="grid grid-cols-[260px_1fr] h-screen">
		<div class="flex flex-col border-r h-full">
			<div class="h-14 border-b flex items-center">
				<HomeLink class="w-full h-full pl-3" />
			</div>
			<div class="flex flex-col space-y-1 p-3">
				<NuxtLink
					v-for="nav in navs"
					:to="nav.path"
					class="p-2 rounded-md hover:bg-slate-100">
					{{ nav.name }}
				</NuxtLink>
			</div>
		</div>
		<div>
			<div class="h-14 border-b px-3"></div>
			<NuxtPage />
		</div>
	</div>
</template>

<style scoped></style>
