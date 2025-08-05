<script>
	let { data } = $props();
</script>

<div
	class="flex items-center justify-center text-center h-screen bg-gray-950 text-gray-100 font-sans p-8"
>
	<div class="max-w-4xl">
		<!-- {#if $user}
			<h1 class="text-5xl md:text-7xl font-extrabold mb-4 text-white">¡Bienvenido de nuevo!</h1>
			<p class="text-xl md:text-2xl font-light mb-8 text-gray-400">
				Estás listo para empezar. Explora tus proyectos.
			</p>
			<a
				href="/dashboard"
				class="inline-block px-8 py-4 text-lg font-semibold text-white bg-gray-800 rounded-lg shadow-lg hover:bg-gray-700 transition-transform transform hover:-translate-y-1 focus:outline-none focus:ring-4 focus:ring-gray-600 focus:ring-opacity-50"
			>
				Ir al Panel de Control
			</a>
		{:else} -->
		<h1 class="text-5xl md:text-7xl font-extrabold mb-4 text-white">
			Inicia sesión y empieza a crear
		</h1>
		<p class="text-xl md:text-2xl font-light mb-8 text-gray-400">
			La forma más rápida de construir tu aplicación con SvelteKit y Supabase.
		</p>
		<a
			href="/login"
			class="inline-block px-8 py-4 text-lg font-semibold text-white bg-gray-800 rounded-lg shadow-lg hover:bg-gray-700 transition-transform transform hover:-translate-y-1 focus:outline-none focus:ring-4 focus:ring-gray-600 focus:ring-opacity-50"
		>
			Comenzar
		</a>
		<!-- {/if} -->

		<ul class="mt-8 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
			{#each data.instruments as instrument}
				<li
					class="transform cursor-pointer rounded-lg bg-gray-800/50 p-4 font-semibold text-gray-200 transition-colors duration-200 hover:text-purple-400 hover:bg-gray-700/50"
				>
					{instrument.name}
				</li>
			{/each}
		</ul>
	</div>
</div>
