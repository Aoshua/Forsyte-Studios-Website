<script setup lang="ts">
	import ProductCarousel from "./components/ProductCarousel.vue"
</script>

<template>
	<div class="fixed inset-0 h-full w-full bg-[url('/img/wallpaper.jpg')] bg-cover bg-center bg-fixed z-0"></div>
	<div class="relative z-10 min-h-screen w-full flex justify-center items-start overflow-y-auto text-white">
		<div class="space-y-6 lg:space-y-10 bg-gray-900/60 p-3 sm:p-4 md:p-6 lg:rounded-xl lg:my-4 w-full max-w-xl sm:max-w-2xl md:max-w-3xl lg:max-w-4xl">
			<div class="flex justify-center">
				<div class="flex flex-col gap-3 lg:gap-0 items-center">
					<div class="h-20 w-20 md:h-40 md:w-40 -mb-6 -mt-3 lg:mt-0 bg-[url('/img/logo-white.png')] bg-cover bg-center"></div>
					<div class="text-3xl lg:text-6xl bruno-ace-sc-regular">Forsyte Studios</div>
				</div>
			</div>
			<ProductCarousel />
			<div class="space-y-2">
				<div class="text-xl sm:text-2xl md:text-3xl">Our Mission</div>
				<p class="text-base sm:text-lg md:text-xl max-w-full">
					We create imaginative, accessible digital experiences that bring people together through play. We focus on crafting polished, innovative games and apps — from
					classic platformers to unique real-world AR adventures — with the goal of sharing creativity and inspiring connection across devices and communities.
				</p>
			</div>
			<div class="space-y-2">
				<div class="text-xl sm:text-2xl md:text-3xl">Contact Us</div>
				<a class="text-base sm:text-lg md:text-xl" href="mailto:forsyte.studios@gmail.com">forsyte.studios@gmail.com</a>
			</div>
		</div>
	</div>
</template>

<style scoped>
	/* Prevent content overflow and ensure scrolling over static background */
	body,
	#app {
		min-height: 100vh;
		margin: 0;
		padding: 0;
		overflow: hidden;
	}
	.relative {
		overflow-y: auto;
	}

	.bruno-ace-sc-regular {
		font-family: "Bruno Ace SC", sans-serif;
		font-weight: 400;
		font-style: normal;
	}
</style>
