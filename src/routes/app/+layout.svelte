<script>
	import Header from '$lib/components/header.svelte';
	import CreatePostModal from '$lib/components/createPostModal.svelte';

	let isPostModalOpen = false;
	function togglePostModal() {
		isPostModalOpen = !isPostModalOpen;
	}
</script>

<div class="flex h-screen">
	<Header />
	<div class="flex-auto bg-gray-50 p-4 overflow-y-auto">
		<slot />
	</div>
</div>

<!-- Floating Action Button -->
<a class="fab" href="/app/createPost">
	<span class="text-xl">+</span>
</a>


{#if isPostModalOpen}
  <CreatePostModal on:close={() => isPostModalOpen=false} />
{/if}
<style>
	.fab {
		position: fixed;
		bottom: 30px;
		right: 30px;
		z-index: 1000;
		background-color: #262626;
		color: white;
		border-radius: 50%;
		width: 60px;
		height: 60px;
		display: flex;
		justify-content: center;
		align-items: center;
		box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
		cursor: pointer;
		transition: transform 0.2s;
	}

	.fab:hover {
		transform: scale(1.1);
	}
</style>
