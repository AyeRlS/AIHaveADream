<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	let mode = 'text';
	let postContent = '';
	let isRecording = false;
	let generatedImages = [];
	let selectedImage;

	async function generateImages() {
		// Simulating API call
		await new Promise((res) => setTimeout(res, 2000));
		generatedImages = ['img1.png', 'img2.png', 'img3.png', 'img4.png']; // Replace with real image URLs
	}

	function post() {
		// Use the `postContent` and `selectedImage` to create a post
		closeModal();
	}

	function closeModal() {
		dispatch('close');
	}
</script>

<div class="create-post-modal fixed inset-0 flex items-center justify-center z-50">
	<div class="bg-white p-10 rounded-lg shadow-xl w-96">
		<span class="close-button absolute top-3 right-3 cursor-pointer">✕</span>
		<h3 class="text-xl font-bold mb-5">Enter your post</h3>

		<!-- Text Input -->
		<textarea
			class="post-input border border-gray-300 p-2 w-full rounded mb-5"
			rows="4"
			placeholder="Enter content here..."
		/>

		<!-- Audio Recording -->
		<button
			class="record-audio-button bg-red-500 text-white px-5 py-2 rounded hover:bg-red-600 mb-5"
		>
			Record Audio
		</button>

		<!-- Media Placeholders -->
		<div class="grid grid-cols-2 gap-4 mb-5">
			<div class="media-placeholder bg-gray-200 p-5 rounded flex items-center justify-center">
				Placeholder
			</div>
			<div class="media-placeholder bg-gray-200 p-5 rounded flex items-center justify-center">
				Placeholder
			</div>
			<div class="media-placeholder bg-gray-200 p-5 rounded flex items-center justify-center">
				Placeholder
			</div>
			<div class="media-placeholder bg-gray-200 p-5 rounded flex items-center justify-center">
				Placeholder
			</div>
		</div>

		<!-- Action Buttons -->
		<div class="flex justify-between">
			<button class="generate-button bg-green-500 text-white px-5 py-2 rounded hover:bg-green-600">
				Generate Images
			</button>
			<button class="post-button bg-blue-500 text-white px-5 py-2 rounded hover:bg-blue-600">
				Create Post
			</button>
		</div>
	</div>
</div>
