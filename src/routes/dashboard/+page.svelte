<script lang="ts">
	import { invalidate } from '$app/navigation';
	import type { EventHandler } from 'svelte/elements';

	import type { PageData } from './$types';

	let { data } = $props();
	let { notes, supabase, user } = $derived(data);
	const handleSubmit: EventHandler<SubmitEvent, HTMLFormElement> = async (evt) => {
		evt.preventDefault();
		if (!evt.target) return;
		const form = evt.target as HTMLFormElement;
		const note = (new FormData(form).get('note') ?? '') as string;
		if (!note) return;
		const { error } = await supabase.from('notes').insert({ note });
		if (error) console.error(error);
		invalidate('supabase:db:notes');
		form.reset();
	};
</script>

<div
	class="flex min-h-screen items-center justify-center bg-gradient-to-br from-gray-900 to-black p-6 font-sans text-center text-gray-100"
>
	<div class="w-full max-w-lg space-y-8 rounded-xl bg-gray-800/50 p-10 shadow-xl backdrop-blur-sm">
		<h1 class="text-4xl font-extrabold text-white sm:text-5xl">¡Bienvenido {user?.email}!</h1>
		<p class="text-lg text-gray-400">
			Este es tu dashboard. Desde aquí puedes gestionar tu cuenta.
		</p>

		<button
			class="mt-6 rounded-full border border-red-500 bg-transparent px-8 py-3 text-lg font-semibold text-red-500 transition-colors duration-300 hover:bg-red-500 hover:text-white focus:outline-none focus:ring-2 focus:ring-red-500"
		>
			Cerrar Sesión
		</button>

		<h2 class="text-4xl font-extrabold text-white sm:text-5xl">Notas!</h2>

		<ul class="mt-8 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
			{#each notes as note}
				<li
					class="transform cursor-pointer rounded-lg bg-gray-800/50 p-4 font-semibold text-gray-200 transition-colors duration-200 hover:text-purple-400 hover:bg-gray-700/50"
				>
					{note.note}
				</li>
			{/each}
		</ul>

		<form onsubmit={handleSubmit}>
			<label>
				Add a note
				<input name="note" type="text" class="text-zinc-900" />
			</label>
		</form>
	</div>
</div>
