<script>
	// your script goes here
	import { onMount } from 'svelte';
	import DriftLogo from './DriftLogo.svelte';

	//TODO: Check for Mobile & adapt.
	let show_mobile = false;
</script>

<nav class="">
	<div class="px-10 md:px-20 mx-auto">
		<div class="flex justify-between">
			<!-- Top Left Group -->
			<div class="flex items-center space-x-4">
				<!-- Logo -->
				<div class="text-gray-800">
					<!-- Medium Screens and up -->
					<a class="hidden md:flex items-center py-10 px-2" href="/#">
						<!-- <DriftLogo logo_height_scale={0.3} logo_width_scale={0.3}/> -->
						<svg
							class="h-10 w-10 mr-2 stroke-orange-500"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="2"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M21 7.5l-2.25-1.313M21 7.5v2.25m0-2.25l-2.25 1.313M3 7.5l2.25-1.313M3 7.5l2.25 1.313M3 7.5v2.25m9 3l2.25-1.313M12 12.75l-2.25-1.313M12 12.75V15m0 6.75l2.25-1.313M12 21.75V19.5m0 2.25l-2.25-1.313m0-16.875L12 2.25l2.25 1.313M21 14.25v2.25l-2.25 1.313m-13.5 0L3 16.5v-2.25"
							/>
						</svg>

						<span class="">Marknet</span>
					</a>
					<!-- Mobile -->
					<div class="flex items-center md:hidden py-10 px-2">
						<button class="">
							<svg
								class="h-10 w-10 mr-2 stroke-orange-500"
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="2"
								stroke="currentColor"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M21 7.5l-2.25-1.313M21 7.5v2.25m0-2.25l-2.25 1.313M3 7.5l2.25-1.313M3 7.5l2.25 1.313M3 7.5v2.25m9 3l2.25-1.313M12 12.75l-2.25-1.313M12 12.75V15m0 6.75l2.25-1.313M12 21.75V19.5m0 2.25l-2.25-1.313m0-16.875L12 2.25l2.25 1.313M21 14.25v2.25l-2.25 1.313m-13.5 0L3 16.5v-2.25"
								/>
							</svg>
						</button>
						<span class="">Marknet</span>
					</div>
				</div>

				<!-- Primary Nav -->
				<div class="hidden md:flex space-x-1 text-gray-800">
					<a class="py-5 px-2 hover:text-orange-500" href="/me">me</a>
					<a class="py-5 px-2 hover:text-orange-500" href="/archive">archive</a>
				</div>
			</div>

			<!-- Secondary Nav (Top Right) -->
			<div class="hidden md:flex items-center space-x-1 text-gray-800">
				<a class="py-5 px-2 hover:text-orange-500" href="/contact">contact</a>
				<a class="py-5 px-2 hover:text-orange-500" href="/test">test</a>
			</div>

			<!-- Mobile -->
		</div>
	</div>
</nav>
