<script>
	// @ts-nocheck
	import { page } from '$app/stores';

	const emojis = {
		// TODO add the rest!
		420: '🫠',
		500: '💥'
	};
</script>

<div class="py-44 md:py-44">
	<span>
		<h1 class="font-black text-3xl md:text-8xl">{emojis[$page.status] ?? emojis[500]} {$page.status}</h1>
		<h2 class="font-black text-3xl md:text-8xl">{$page.error.message}</h2>
		<span class="font-extrabold text-3xl md:text-9xl">
		Oh no!
		</span>
	</span>
</div>

