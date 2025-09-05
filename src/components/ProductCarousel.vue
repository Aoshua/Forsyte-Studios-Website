<script setup lang="ts">
	import { ref, onMounted, onUnmounted } from "vue"

	const images = ["/img/products/green-squario.png", "/img/products/run-io.png"]
	const current = ref(0)
	let interval: number | undefined

	function next() {
		current.value = (current.value + 1) % images.length
	}
	function prev() {
		current.value = (current.value - 1 + images.length) % images.length
	}
	function goTo(idx: number) {
		current.value = idx
	}

	onMounted(() => {
		interval = window.setInterval(next, 7000)
	})
	onUnmounted(() => {
		if (interval) window.clearInterval(interval)
	})
</script>

<template>
	<div class="w-50 lg:w-96 mx-auto flex flex-col items-center">
		<div class="relative w-full h-50 lg:h-96 overflow-hidden rounded-lg mb-4">
			<img :src="images[current]" alt="carousel" class="w-full h-full object-cover transition duration-500" />
		</div>
		<div class="flex gap-4 items-center justify-center w-full">
			<div class="flex gap-2">
				<button
					v-for="(img, idx) in images"
					:key="idx"
					@click="goTo(idx)"
					:class="['w-3 h-3 rounded-full', current === idx ? 'bg-white' : 'bg-gray-400']"
					aria-label="Go to slide"
				></button>
			</div>
		</div>
	</div>
</template>

<style scoped lang="less"></style>
