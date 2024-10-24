<script>
	import { WandSparkles } from 'lucide-svelte';
	import Logo from "$lib/logo.svelte";
	let showLogo = true
</script>


<div id="top-blob" class="absolute top-[-15rem] left-0 right-0 ml-auto mr-auto w-[80vw] h-[20rem] rounded-[50%] bg-gradient-to-br from-surface-500 via-primary-500 to-white opacity-40 overflow-x-hidden blur-3xl" >
</div>



<div class="container h-screen w-auto mx-auto flex justify-center items-center text-center bg-black overflow-hidden">
	<div class="w-auto">
		<!--
			<h1 class="h1 text-[3in]">GLO</h1>
		-->
		<span class="badge variant-ghost px-6 py-2 text-lg text-[1rem] transition-shadow duration-300 hover:shadow-xl hover:shadow-[#ffffff80] select-none"><WandSparkles class="mr-2"/>Coming Soon</span>
		

		<Logo show = {showLogo}/>


		
		<h2 class="mt-4 tracking-tighter text-2xl bg-gradient-to-b from-white via-white to-gray-500 inline-block text-transparent bg-clip-text font-extrabold text-center relative z-20">Where your cosmetics <span class="gradient-hero">come to you</span></h2>
		
		<!--
			Inspired by carbon.host
		-->
		<div class="w-[40rem] relative mt-10">
			<div class="absolute inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-[2px] w-3/4 blur-sm"></div>
			<div class="absolute inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-px w-3/4"></div>
			<div class="absolute inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-[5px] w-1/4 blur-sm"></div>
			<div class="absolute inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-px w-1/4"></div>
		</div>


	
	</div>
</div>
