<script>
	import { goto } from '$app/navigation';
	import SimpleCard from '$lib/components/SimpleCard.svelte';

	//TODO: Fetch Projects from an API dynamically
	//Dummy Data 4 Mockups
	const projects = ['Sample1', 'Sample2', 'Sample3', 'Sample4'];
</script>

<!-- TODO: ARCHIVE LAYOUT -->
<!-- Sample of the basic idea for the archive view -->
<div  class="flexbox space-y-2 border border-red-500">
	{#each projects as p}
		<!-- content here -->
		<SimpleCard>
			<div slot="heading">
				{p}
			</div>
		</SimpleCard>
	{/each}
</div>
