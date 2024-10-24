<script>
	import { fade } from "svelte/transition";

  export let show = false
</script>

{#if show}
<div class="relative w-auto" transition:fade>
  <h1 class="text-[2.75in] gradient-hero leading-normal font-[bumbbled] whitespace-nowrap select-none">
    Glo
  </h1>
  <h1 class="text-[2.75in] gradient-hero leading-normal font-[bumbbled] blur-lg absolute inset-0 whitespace-nowrap select-none">
    Glo
  </h1>
</div>


{/if}