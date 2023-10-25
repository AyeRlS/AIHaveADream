<script lang="ts">
	import Post from "$lib/components/post.svelte";

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
</script>

<div class="grid grid-cols-1 gap-4">
	{#each images as image}
	  <Post image={{
		src: image.url,
		likes: 142,
		username: 'lucilleppp',
		caption: image.caption,
	  }} />
	{/each}
</div>
