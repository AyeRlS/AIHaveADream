<script lang="ts">
	import Post from '$lib/components/post.svelte';

	const images = [
		// {
		// 	id: -2,
		// 	url: 'img.jpg',
		// 	caption: 'Enjoying the sunshine!',
		// },
		// {
		// 	id: -1,
		// 	url: 'img.jpg',
		// 	caption: 'Enjoying the sunshine!',
		// },
		{
			id: 0,
			url: 'https://picsum.photos/id/523/1000/1000',
			caption: 'Enjoying the sunshine!'
		},
		{
			id: 1,
			url: 'https://picsum.photos/id/337/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 2,
			url: 'https://picsum.photos/id/238/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 3,
			url: 'https://picsum.photos/id/137/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 4,
			url: 'https://picsum.photos/id/287/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 5,
			url: 'https://picsum.photos/id/217/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 6,
			url: 'https://picsum.photos/id/227/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 7,
			url: 'https://picsum.photos/id/247/1000/1000',
			caption: 'Enjoying the sunshine!'
		},
		{
			id: 8,
			url: 'https://picsum.photos/id/257/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 9,
			url: 'https://picsum.photos/id/267/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 10,
			url: 'https://picsum.photos/id/537/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 11,
			url: 'https://picsum.photos/id/437/1000/1000',
			caption: 'Just chilling'
		},		{
			id: 0,
			url: 'https://picsum.photos/id/837/1000/1000',
			caption: 'Enjoying the sunshine!'
		},
		{
			id: 1,
			url: 'https://picsum.photos/id/637/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 2,
			url: 'https://picsum.photos/id/137/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 3,
			url: 'https://picsum.photos/id/217/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 4,
			url: 'https://picsum.photos/id/231/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 5,
			url: 'https://picsum.photos/id/937/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 6,
			url: 'https://picsum.photos/id/297/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 7,
			url: 'https://picsum.photos/id/239/1000/1000',
			caption: 'Enjoying the sunshine!'
		},
		{
			id: 8,
			url: 'https://picsum.photos/id/147/1000/1000',
			caption: 'What a wonderful day!'
		},
		{
			id: 9,
			url: 'https://picsum.photos/id/134/1000/1000',
			caption: 'I love this view!'
		},
		{
			id: 10,
			url: 'https://picsum.photos/id/135/1000/1000',
			caption: 'Just chilling'
		},
		{
			id: 11,
			url: 'https://picsum.photos/id/157/1000/1000',
			caption: 'Just chilling'
		},
	];

	// Default size
	let imageSize = '250px';
</script>

<div class="grid grid-cols-5 gap-4">
	{#each images as image}
		<div
			class="mx-auto border rounded overflow-hidden shadow-lg bg-white"
			style={`width: ${imageSize};`}
		>
			<div class="image-container" style={`--image-size: ${imageSize};`}>
				<img src={image.url} alt="Instagram post image" />
			</div>
		</div>
	{/each}
</div>

<style>
	.hover-caption {
		transition: opacity 0.3s ease-in-out;
	}

	.image-container {
		width: var(--image-size, 400px);
		height: var(--image-size, 400px);
		overflow: hidden;
		position: relative;
	}

	.image-container img {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
