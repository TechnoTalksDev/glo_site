<script>
	import { ArrowDown, WandSparkles } from 'lucide-svelte';
	import { blur, fade, scale } from 'svelte/transition';
	import { onMount } from 'svelte';
	import Particles from '$lib/Particles.svelte';
	import ProjectCard from '$lib/projectCard.svelte';
	import GenerateText from '$lib/generateText.svelte';

	let animate = false;
	let showProjectCard = false;
	/**
	 * @type {number}
	 */
	let scrollY;

	onMount(() => {
		animate = true;
	});

	// Function to check scroll position and show project card
	function handleScroll() {
		// Show project card when user scrolls a bit (e.g., 100px)
		showProjectCard = scrollY > 100;
	}

	const projects = [
		{
			name: 'Reko',
			img: '/reko-banner.png',
			description:
				'Discord bot integration for Minecraft servers. Monitor through panels, charts, and more.',
			link: '',
			github: 'https://github.com/TechnoTalksDev/Reko',
			tags: ['Discord', 'API', 'Minecraft', 'Server']
		},
		{
			name: 'HotDash',
			img: '/hot-dash.png',
			description: 'Simple dashboard for host temperatures and load',
			link: '',
			github: 'https://github.com/TechnoTalksDev/HotDash',
			tags: ['Server', 'Docker']
		},
		{
			name: '10A VEX',
			img: '/10A.png',
			description:
				'VEX V5 Robotics programming, implementing various motion algorithms, telemetry systems, localization, and more.',
			link: '',
			github: 'https://github.com/Exo10A',
			tags: ['VEX', ['c++']]
		},
		/*
		{
			name: "Retrospective",
			img: "https://fastrepair.biz/wp-content/uploads/2018/10/iStock-984996502-3.jpg",
			description: "Built by students for students",
			link: "",
			github: "",
			tags: ["startup"]
		},
		*/
		{
			name: 'Simeo',
			img: '/simeo_full.png',
			description:
				'GPA and Grade caluculation for Synergy students. With seamless integration with Synergy, and highly customizable calculations.',
			link: 'https://www.simeo.app/',
			github: 'https://github.com/TechnoTalksDev/Simeo',
			tags: ['FBLA', 'full-stack']
		},
		{
			name: 'Reko Link',
			img: '/reko-banner.png',
			description:
				'Integration server-side for Reko with WebSockets, API, and more. Allowing access to server console, 2 way chat, active roles, and more.',
			link: '',
			github: 'https://github.com/TechnoTalksDev/Reko-Link',
			tags: ['WebSockets', 'API', 'Minecraft', 'Server']
		},
		{
			name: 'Rider-MC',
			img: '/rider-banner.png',
			description: 'Ride any Minecraft mob! With a variety of permissions, and customization.',
			link: 'https://www.spigotmc.org/resources/rider-simple-easy-ride-anything-1-8x-1-17x.93807/',
			github: 'https://github.com/TechnoTalksDev/Rider-MC',
			tags: ['Minecraft', 'Plugin', 'Java']
		},
		{
			name: 'CraftableSaddlesMC',
			img: '/saddle-banner.png',
			description: 'Craft saddles for any mob! With a variety of permissions, and customization.',
			link: 'https://www.spigotmc.org/resources/craftablesaddles-simple-easy-1-8x-1-17x.93871/',
			github: 'https://github.com/TechnoTalksDev/CraftableSaddlesMC',
			tags: ['Minecraft', 'Plugin', 'Java']
		},
		{
			name: 'Spaceboi',
			img: '/spaceboi.png',
			description: 'Pilot and fight in 2D! Built with pygame, and python.',
			link: '',
			github: 'https://github.com/TechnoTalksDev/Spaceboi',
			tags: ['PyGame', 'Python', 'GameDev']
		},
		{
			name: 'SAHF',
			img: '/SAHF-banner.png',
			description:
				'South Asian Heart Foundation website, featuring a variety of services, along with a blog.',
			link: 'https://www.sahf.life/',
			github: 'https://github.com/South-Asian-Heart-Foundation/SAHF-site',
			tags: ['SvelteKit', 'full-stack', 'Non-profit']
		}
	];

	const featuredProject= {name: "Simeo", description: "A GPA and Grade solution for Synergy students", tags: ["FBLA", "full-stack"], link: "https://www.simeo.app/", github: "https://github.com/TechnoTalksDev/Simeo", img: "/simeo_full.png"}
</script>

<svelte:window bind:scrollY={scrollY} on:scroll={handleScroll}/>

<!-- Main container allowing scrolling but preventing x overflow -->
<div class="relative w-screen h-screen overflow-y-auto overflow-x-hidden">
	<!-- Initial hero section - roughly 100vh tall -->
	<div class="w-full h-screen flex items-center justify-center">
		{#if animate}
			<div
				id="top-blob"
				transition:blur={{ amount: 5, duration: 1500 }}
				class="absolute top-[-15rem] left-0 right-0 ml-auto mr-auto w-[80vw] h-[20rem] rounded-[50%] bg-gradient-to-br from-surface-500 via-primary-500 to-white opacity-40 overflow-x-hidden blur-3xl"
			></div>

			<div
				class="container h-full w-full mx-auto flex justify-center items-center text-center bg-black overflow-visible"
			>
				<Particles
					className="absolute inset-0 -z-5 opacity-50"
					refresh={true}
					staticity={30}
					quantity={250}
				/>
				<div class="w-auto">
					<!--
					<h1 class="h1 text-[3in]">GLO</h1>
					-->
					<a href="https://www.technotalks.net/" target="_blank">
						<span
							transition:fade={{ delay: 1000, duration: 1000 }}
							class="scale-[80%] md:scale-[100%] badge w-fit variant-ghost px-6 py-2 text-lg text-[1rem] transition-shadow duration-300 hover:shadow-lg hover:shadow-[#ffffff80] select-none"
							><WandSparkles class="mr-2" />Coming Soon</span
						>
					</a>

					<div
						class="relative w-full max-w-none overflow-visible"
						transition:blur={{ amount: 5, duration: 1500 }}
						style="-webkit-text-fill-color: transparent;"
					>
						<h1
							class="text-[15vw] md:text-[1.5in] gradient-hero leading-normal font-[bumbbled] whitespace-nowrap select-none"
						>
							retrospective
						</h1>

						<h1
							class="text-[15vw] md:text-[1.5in] gradient-hero leading-normal font-[bumbbled] blur-lg absolute inset-0 whitespace-nowrap"
						>
							retrospective
						</h1>
					</div>

					<h2
						transition:fade={{ delay: 750, duration: 500 }}
						class="mt-4 tracking-tighter text-[5vw] md:text-3xl bg-gradient-to-b from-white via-white to-gray-500 inline-block text-transparent bg-clip-text font-extrabold text-center relative z-20 leading-[1.3]"
						style="-webkit-text-fill-color: transparent;"
					>
						Built by students for <span class="gradient-hero">students</span>
					</h2>

					<!--
					Carbon bar
					Inspired by carbon.host
					-->
					<div class="w-full flex items-center justify-center">
						<div class="w-[98vw] md:w-[40rem] relative mt-10" transition:scale={{ delay: 750 }}>
							<div
								class="absolute inset-x-[5%] md:inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-[2px] w-[90%] md:w-3/4 blur-sm"
							></div>
							<div
								class="absolute inset-x-[5%] md:inset-x-20 top-0 bg-gradient-to-r from-transparent via-orange-500 to-transparent h-px w-[90%] md:w-3/4"
							></div>
							<div
								class="absolute inset-x-[30%] md:inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-[5px] w-[40%] md:w-1/4 blur-sm"
							></div>
							<div
								class="absolute inset-x-[30%] md:inset-x-60 top-0 bg-gradient-to-r from-transparent via-red-500 to-transparent h-px w-[40%] md:w-1/4"
							></div>
						</div>
					</div>
					
					<div class="w-full flex items-center justify-center mt-6 " transition:fade={{ delay: 1300, duration: 1000 }}>
						<a href="https://www.instagram.com/retrospective.tech/" target="_blank">
							<img
								src="/instagram.svg"
								alt="insta"
								class="w-[2.5rem] aspect-square saturate-[80%] transform-gpu hover:scale-110 hover:saturate-100 transition-all duration-500" />
						</a>
					</div>
					
					<!-- Hint to scroll down 
					
					<div class="mt-20 animate-bounce text-white/50">
						<p>Scroll down to see projects</p>
						<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
						</svg>
					</div>
					-->

				</div>

				
			</div>
		{/if}
	</div>

	<!-- Project card section visible on scroll -->
	{#if showProjectCard && animate}
		<div class="min-h-screen h-fit w-full bg-black pt-10 overflow-x-hidden" transition:fade={{ duration: 500 }}>
			<ProjectCard projects={projects} featuredProject={featuredProject} />
		</div>
	{/if}
</div>

<style>
	/*
* { 
  outline: 1px solid red;
  outline-offset: -1px;
}
*/

	/* Ensure no horizontal overflow for the entire page */
	:global(body) {
		overflow-x: hidden;
		max-width: 100vw;
	}

	:global(html) {
		overflow-x: hidden;
		max-width: 100vw;
	}
</style>
