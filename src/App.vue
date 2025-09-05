<script setup lang="ts">
	import ProductCarousel from "./components/ProductCarousel.vue"
</script>

<template>
	<div class="h-dvh w-dvw bg-[url('/img/wallpaper.jpg')] bg-cover bg-center text-white flex justify-center lg:items-center">
		<div class="space-y-10 bg-gray-900/50 p-3 lg:p-6 rounded-xl">
			<div class="flex gap-3 items-center">
				<div class="h-20 w-20 bg-white/90 rounded-xl">
					<div class="w-full h-full bg-[url('/img/logo.png')] bg-cover bg-center"></div>
				</div>
				<div class="text-4xl lg:text-6xl font-semibold">Forsyte Studios</div>
			</div>
			<ProductCarousel />
			<div class="space-y-2">
				<div class="text-3xl">Our Mission</div>
				<p class="text-xl max-w-[40rem]">
					We create imaginative, accessible digital experiences that bring people together through play. We focus on crafting polished, innovative games and apps — from
					classic platformers to unique real-world AR adventures — with the goal of sharing creativity and inspiring connection across devices and communities.
				</p>
			</div>
			<div class="space-y-2">
				<div class="text-3xl">Contact Us</div>
				<a class="text-xl" href="mailto:forsyte.studios@gmail.com">forsyte.studios@gmail.com</a>
			</div>
		</div>
	</div>
</template>

<style scoped></style>
