<script>
	// @ts-nocheck
	import { goto } from '$app/navigation';
	import SimpleCard from '$lib/components/SimpleCard.svelte';
	
	//TODO: Add Markdown Content Import

</script>

<SimpleCard>
	<div slot="heading"><h1>Contact Details</h1></div>
	<div slot="body">
		<span>---</span>
        <br>
        <span>TODO: socials cards</span>
	</div>
	<div slot="btn">
		<button
			on:click={() => {
				goto('/');
			}}
			class="hover:-translate-y-0.5 transition-transform text-xl"
		>
			&times;
		</button>
	</div>
</SimpleCard>