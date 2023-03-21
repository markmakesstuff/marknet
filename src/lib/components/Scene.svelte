<script>
	import { T, useFrame } from '@threlte/core';
	import { interactivity } from '@threlte/extras';
	import { spring } from 'svelte/motion';
	import { model } from '../../stores';

	interactivity();
	const scale = spring(1);
	let rotation = 0;
	useFrame((state, delta) => {
		rotation += delta * 0.5;
	});
</script>

<T.PerspectiveCamera
	makeDefault
	position={[10, 10, 10]}
	on:create={({ ref }) => {
		ref.lookAt(0, 1, 0);
	}}
/>

<T.DirectionalLight position={[3, 10, 7]} />

<T.Mesh
	rotation.y={rotation}
	position.y={1}
	scale={3 * $scale}
	on:pointerenter={() => scale.set(1.5)}
	on:pointerleave={() => scale.set(1)}
>
{#if $model === 'model1'}
   <!-- content here -->  
   <T.SphereGeometry args={[1.5, 10, 10]} />
{:else if  $model === 'model2'}
   <!-- else if content here -->
   <T.BoxGeometry args={[1, 1, 1]} />
{:else if $model === 'model3'}
   <!-- else content here -->
   <T.SphereGeometry args={[1.5, 3, 6]} />
{:else}
  <!-- fallback -->
  <T.SphereGeometry args={[2, 10, 10]} />
{/if}
	<T.MeshBasicMaterial color="grey" wireframe={true} />
</T.Mesh>
