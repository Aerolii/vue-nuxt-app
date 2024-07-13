<script setup lang="ts"></script>

<template>
	<label class="w-full inline-block text-black/40 font-light text-sm">
		<input
			type="text"
			name="todo"
			id="todoIpt"
			placeholder="What needs to be done?"
			class="w-full border border-slate-300 outline-none hover:bg-slate-50/10 transition-all duration-150 ease-linear hover:border-slate-400 rounded-md h-10 indent-2 focus:border-red-300 active:border-red-300"
			v-bind="$attrs" />
		<span class="indent-1 mt-1 inline-block">Press Enter keyboard to add.</span>
	</label>
</template>

<style scoped></style>
