<script>
	import { WandSparkles } from 'lucide-svelte';

	import {
		blur,
		fade,
		scale,

	} from 'svelte/transition';

	import { onMount } from 'svelte';

	let animate = false

	onMount(() => {
		animate = true
	})

</script>


{#if animate}
<div id="top-blob" transition:blur = {{amount: 5, duration: 1500}} class="absolute top-[-15rem] left-0 right-0 ml-auto mr-auto w-[80vw] h-[20rem] rounded-[50%] bg-gradient-to-br from-surface-500 via-primary-500 to-white opacity-40 overflow-x-hidden blur-3xl" >
</div>


<div class="container h-screen w-auto mx-auto flex justify-center items-center text-center bg-black overflow-hidden">
	<div class="w-auto">
		<!--
			<h1 class="h1 text-[3in]">GLO</h1>
		-->
		<a href="https://www.technotalks.net/" target="_blank">
		<span transition:fade = {{delay: 1000, duration: 1000}} class="scale-[80%] md:scale-[100%] badge w-fit variant-ghost px-6 py-2 text-lg text-[1rem] transition-shadow duration-300 hover:shadow-lg hover:shadow-[#ffffff80] select-none"><WandSparkles class="mr-2"/>Coming Soon</span>
	</a>

		<div class="relative w-auto" transition:blur = {{amount: 5, duration: 1500}}>
			
			<h1 class="text-[15vw] md:text-[1.5in] gradient-hero leading-normal font-[bumbbled] whitespace-nowrap select-none">
				retrospective
			</h1>

			
			<h1 class="text-[15vw] md:text-[1.5in] gradient-hero leading-normal font-[bumbbled] blur-lg absolute inset-0 whitespace-nowrap">
				retrospective
			</h1>
			
		</div>


		
		<h2 transition:fade = {{delay: 750, duration: 500}} class="mt-4 tracking-tighter text-[6vw] md:text-3xl bg-gradient-to-b from-white via-white to-gray-500 inline-block text-transparent bg-clip-text font-extrabold text-center relative z-20">Built by students for <span class="gradient-hero">students</span></h2>
		
		<!--
			Inspired by carbon.host
		-->
		<div class="w-full flex items-center justify-center">
		<div class="w-[40rem] relative mt-10" transition:scale = {{delay: 750}}>
			<div class="absolute inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-[2px] w-3/4 blur-sm"></div>
			<div class="absolute inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-px w-3/4"></div>
			<div class="absolute inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-[5px] w-1/4 blur-sm"></div>
			<div class="absolute inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-px w-1/4"></div>
		</div>
		</div>

	
	</div>
</div>
{/if}

