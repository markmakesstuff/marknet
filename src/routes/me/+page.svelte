<script>
	// @ts-nocheck
	import { goto } from '$app/navigation';
	import SimpleCard from '$lib/components/SimpleCard.svelte';
	
	//TODO: Add Markdown Content Import

</script>

<SimpleCard>
	<div slot="heading"><h1>Who Am I?</h1></div>
	<div slot="body">
		<span>---</span>
		<p>
			Hi, <br />Welcome to my website Marknet. My name is Mark as you might have guessed. I enjoy
			exploring interesting ideas and creaating things, this site is meant as a home for some of
			that.
			<br /> <br />A bit about me:
		</p>
		<ul>
			<li>- Factoid</li>
			<li>- Factoid</li>
			<li>- Factoid</li>
			<li>- Factoid</li>
			<li>- Factoid</li>
			<li>- Factoid</li>
		</ul>
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
