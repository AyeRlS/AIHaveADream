<script>
	export let image = {
		src: '',
		likes: 0,
		username: '',
		caption: ''
	};

	let isHovered = false;

	// Default size
	let imageSize = '600px';
</script>

<div
	class="mx-auto mt-10 border rounded overflow-hidden shadow-lg bg-white"
	style={`width: ${imageSize};`}
>
	<div class="p-4 flex justify-between items-center border-b">
		<span class="font-bold text-lg">{image.username}</span>
	</div>
	<div
		class="image-container"
		on:mouseover={() => (isHovered = true)}
		on:mouseout={() => (isHovered = false)}
		style={`--image-size: ${imageSize};`}
	>
		<img src={image.src} alt="Instagram post image" />
		<div
			class="absolute bottom-0 w-full p-4 hover-caption"
			style={`opacity: ${isHovered ? 1 : 0}; background: rgba(0,0,0,0.5); color: white;`}
		>
			<span class="font-bold">{image.username} </span>
			<span>{image.caption}</span>
		</div>
	</div>
	<div class="p-4">
		<div class="flex items-center">
			<span class="mr-2 text-red-500">❤️</span>
			<span class="font-semibold">{image.likes} likes</span>
		</div>
	</div>
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
