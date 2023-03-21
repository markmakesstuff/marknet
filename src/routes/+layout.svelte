<script>
	import { Canvas } from '@threlte/core';
	import Scene from '$lib/components/Scene.svelte';
	import LeftHUD from '$lib/components/LeftHUD.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import { page } from '$app/stores';
	import { model } from '../stores.js'
	import '../app.css';

	const { url, params } = $page;
	//load func props
	/**
	 * @type {{ title: string; }}
	 */
	export let data;

	$model = 'm1'

</script>

<svelte:head>
	<!-- head content -->
	<!-- TODO: More SEO Shit -->
	<title>{data.title}</title>
</svelte:head>

<!-- NOTE: bundling slot with nav may prove problematic, as some components injected may need to be relative rather than fixed -->
<div class="nav z-10 w-full fixed">
	<Nav />
</div>

<div
	class="content-container z-9 fixed w-full flexbox justify-between py-32 px-14 md:px-40 lg:px-80"
>
	<slot>Loading...</slot>
</div>

<div class="canvas-container flex justify-between py-20 px-0 h-screen ">
	<div class="w-full">
		<Canvas>
			<Scene />
		</Canvas>
	</div>
</div>

<!-- content here -->
<div class="hudL-SM md:hudL-MD fixed px-20 text-gray-700 font-thin">
	<LeftHUD
		on:tabClicked={(e) => {
			$model = e.detail.text;
		}}
		tabs={['model1', 'model2', 'model3', 'model4']}
	/>
</div>
