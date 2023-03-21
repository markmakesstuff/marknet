<script>
	// @ts-nocheck
	import { page } from '$app/stores';
	import SimpleCard from '$lib/components/SimpleCard.svelte';

	const emojis = {
		// TODO add the rest!
		420: '🫠',
		500: '💥'
	};
</script>

<SimpleCard>
	<div slot="body" class="flex justify-left align-middle space-x-40">
		<div class="py-44 md:py-44 flexbox">
			<span class="font-extrabold text-3xl md:text-9xl"> Oh no! </span>
			<h1 class="font-black text-3xl md:text-8xl">
				{emojis[$page.status] ?? emojis[500]}
				{$page.status}
			</h1>
			<h2 class="font-black text-3xl md:text-4xl">{$page.error.message}</h2>
		</div>
		<div>
			<button class="border border-red-500 max-h-40">
				<a href="/#" class="">
					<span class="font-black text-3xl md:text-8xl border border-red-500">
						Home
					</span>
				</a>
			</button>
		</div>

	</div>
</SimpleCard>
