<script>
	let activeItem = 'Home'; // Default active item

	const links = [
		{
			name: 'Home',
			url: '/app/',
			icon: 'home'
		},
		{
			name: 'Explore',
			url: '/app/explore',
			icon: 'compass'
		},
		{
			name: 'Profile',
			url: '/app/profile',
			icon: 'user'
		}
	];
</script>

<aside class="w-64 bg-white shadow-lg p-6 flex flex-col overflow-y-auto">
	<!-- Logo Section -->
	<div class="mb-8 flex justify-center">
		<h1 class="text-3xl font-bold text-gray-800 tracking-wider">
			Insta<span class="text-red-500">App</span>
		</h1>
	</div>

	<!-- Navigation items -->
	<nav class="flex-grow">
		{#each links as link}
			<a
                href="{link.url}"
				class="nav-item block w-full py-2 mb-2 text-left px-4 {activeItem === link.name
					? 'active-nav-item'
					: 'text-gray-600'}"
				on:click={() => (activeItem = link.name)}
			>
				{link.name}
			</a>
		{/each}
	</nav>

	<!-- Divider -->
	<hr class="my-4 border-t border-gray-300" />

	<!-- Logout option at the bottom -->
	<button class="logout block w-full py-2 text-gray-600 text-left px-4"> Logout </button>
</aside>

<style>
	.nav-item:hover {
		background-color: #f5f5f5;
		border-radius: 12px;
	}

	.active-nav-item {
		color: white;
		background-color: #262626;
		border-radius: 12px;
	}

	.logout:hover {
		background-color: #f5f5f5;
		border-radius: 12px;
	}
</style>
