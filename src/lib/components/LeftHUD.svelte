<script>
	// @ts-nocheck

	import { createEventDispatcher } from 'svelte';
	// TODO: Props for dynamic tabs creation
	/**
	 * @type {String[]}
	 */
	export let tabs;

	const dispatch = createEventDispatcher();

	/**
	 * @param {string} tab
	 */
	function left_hud_event(tabName) {
		dispatch('tabClicked', {
			text: tabName
		});
	}
</script>

<div class="">
	<div class="flex items-center justify-evenly space-x-10">
		{#each tabs as tab}
			<span>
				<button on:click={left_hud_event(tab)} class="hover:-translate-y-0.5 transition-transform text-xl">
					{tab}
				</button>
			</span>
		{/each}
	</div>
</div>
