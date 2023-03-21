<div class="bg-gray-200 bg-opacity-70 rounded-lg px-10 py-10 flexbox relative">
	<slot class="font-bold" name="heading" />
	<slot class="" name="body" />
	<!-- optional insert for top right x or whatever -->
	<div class="absolute top-2 right-4">
		<slot name="btn" />
	</div>
</div>
