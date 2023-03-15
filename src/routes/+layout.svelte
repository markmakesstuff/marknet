<script>
	import CanvasComp from '$lib/components/CanvasComp.svelte';
	import LeftHUD from '$lib/components/LeftHUD.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import '../app.css';

	//load func props
	/**
	 * @type {{ title: string; }}
	 */
	export let data;
</script>

<svelte:head>
	<!-- head content -->
	<!-- TODO: More SEO Shit -->
	<title>{data.title}</title>
</svelte:head>

<!-- NOTE: bundling slot with nav may prove problematic, as some components injected may need to be relative rather than fixed -->
<div class="z-10 fixed w-full">
	<Nav />
	<!-- TODO: DYNAMIC MARGINS HERE -->
	<div class="mr-40 ml-40 my-10">
		<slot>Loading...</slot>	
	</div>
</div>

<div class="flex justify-between py-20 px-0 h-screen ">
	<div class=" z-0 w-full">
		<CanvasComp />
	</div>
</div>

<div class="hudL-SM md:hudL-MD fixed px-20 text-gray-700 font-thin">
	<LeftHUD/>	
</div>


