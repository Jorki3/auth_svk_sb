<script>
	export let isLogin = true;

	let title = isLogin ? 'Inicia Sesión' : 'Crea una Cuenta';
	let action = isLogin ? '?/login' : '?/signup';
	let buttonText = isLogin ? 'Entrar' : 'Crear Cuenta';
</script>

<div class="flex min-h-screen items-center justify-center bg-gray-950 p-6">
	<div class="w-full max-w-md space-y-8 rounded-lg bg-gray-900 p-8 shadow-lg">
		<div class="text-center">
			<h1 class="text-3xl font-extrabold text-white">
				{title}
			</h1>
			<p class="mt-2 text-sm text-gray-400">
				{isLogin ? '¿No tienes una cuenta?' : '¿Ya tienes una cuenta?'}
				<a
					href={isLogin ? '/register' : '/login'}
					class="font-medium text-purple-400 hover:text-purple-300"
					>{isLogin ? 'Regístrate' : 'Inicia Sesión'}</a
				>
			</p>
		</div>

		<form class="space-y-6" method="POST" {action}>
			<div>
				<label for="email" class="mb-2 block text-sm font-medium text-gray-300">
					Correo Electrónico
				</label>
				<input
					type="email"
					id="email"
					name="email"
					placeholder="ejemplo@correo.com"
					required
					class="w-full rounded-md border-0 bg-gray-800 p-3 text-gray-100 placeholder-gray-500 shadow-sm ring-1 ring-inset ring-gray-700 transition-colors duration-200 focus:ring-2 focus:ring-purple-500"
				/>
			</div>

			<div>
				<label for="password" class="mb-2 block text-sm font-medium text-gray-300">
					Contraseña
				</label>
				<input
					type="password"
					id="password"
					name="password"
					required
					class="w-full rounded-md border-0 bg-gray-800 p-3 text-gray-100 placeholder-gray-500 shadow-sm ring-1 ring-inset ring-gray-700 transition-colors duration-200 focus:ring-2 focus:ring-purple-500"
				/>
			</div>

			{#if !isLogin}
				<div>
					<label for="confirmPassword" class="mb-2 block text-sm font-medium text-gray-300">
						Confirma tu Contraseña
					</label>
					<input
						type="password"
						id="confirmPassword"
						name="confirmPassword"
						required
						class="w-full rounded-md border-0 bg-gray-800 p-3 text-gray-100 placeholder-gray-500 shadow-sm ring-1 ring-inset ring-gray-700 transition-colors duration-200 focus:ring-2 focus:ring-purple-500"
					/>
				</div>
			{/if}

			<button
				type="submit"
				class="w-full rounded-md bg-purple-600 p-3 font-semibold text-white shadow-sm transition-colors duration-200 hover:bg-purple-500 focus:outline-none focus:ring-2 focus:ring-purple-500"
			>
				{buttonText}
			</button>
		</form>
	</div>
</div>
