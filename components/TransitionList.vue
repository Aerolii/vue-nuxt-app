<script setup lang="ts">
const getInitialItems = () => [1, 2, 3, 4, 5, 6]
const items = reactive(getInitialItems())

const getRandom = () => Math.floor(Math.random() * items.length)

const onRandom = () => {
	const x = getRandom()
	const y = getRandom()
	;[items[x], items[y]] = [items[y], items[x]]
}
</script>

<template>
	<button
		class="border border-slate-200 rounded-md px-2 py-1 hover:bg-slate-100 transition-all"
		@click="onRandom">
		shuffle
	</button>
	<TransitionGroup class="p-0 relative space-y-2" tag="ul" name="fade">
		<li
			v-for="item in items"
			:key="item"
			class="h-8 text-center bg-slate-200 hover:bg-slate-200/60 flex items-center justify-start pl-4 transition-all rounded-md">
			{{ item }}
		</li>
	</TransitionGroup>
</template>

<style scoped>
.fade-move,
.fade-enter-active,
.fade-leave-active {
	transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}

.fade-enter-from,
.fade-leave-to {
	opacity: 0;
	transform: scaleY(0.01) translate(30px, 0);
}

.fade-leave-active {
	position: absolute;
}
</style>
