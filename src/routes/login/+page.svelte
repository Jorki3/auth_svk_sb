<div class="flex min-h-screen items-center justify-center bg-gray-950 p-6">
	<div class="w-full max-w-md space-y-8 rounded-lg bg-gray-900 p-8 shadow-lg">
		<div class="text-center">
			<h1 class="text-3xl font-extrabold text-white">Inicia Sesión</h1>
			<p class="mt-2 text-sm text-gray-400">
				¿No tienes una cuenta? <a
					href="/register"
					class="font-medium text-purple-400 hover:text-purple-300">Regístrate</a
				>
			</p>
		</div>
		<form class="space-y-6" method="POST" action="?/login">
			<div>
				<label for="email" class="mb-2 block text-sm font-medium text-gray-300"
					>Correo Electrónico</label
				>
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
				<label for="password" class="mb-2 block text-sm font-medium text-gray-300">Contraseña</label
				>
				<input
					type="password"
					id="password"
					name="password"
					placeholder="••••••••"
					required
					class="w-full rounded-md border-0 bg-gray-800 p-3 text-gray-100 placeholder-gray-500 shadow-sm ring-1 ring-inset ring-gray-700 transition-colors duration-200 focus:ring-2 focus:ring-purple-500"
				/>
			</div>
			<button
				type="submit"
				class="w-full rounded-md bg-purple-600 p-3 font-semibold text-white shadow-sm transition-colors duration-200 hover:bg-purple-500 focus:outline-none focus:ring-2 focus:ring-purple-500"
			>
				Entrar
			</button>
		</form>
		<div class="relative">
			<div class="absolute inset-0 flex items-center">
				<span class="w-full border-t border-gray-700"></span>
			</div>
			<div class="relative flex justify-center text-xs uppercase">
				<span class="bg-gray-900 px-2 text-gray-500">O continúa con</span>
			</div>
		</div>
		<div class="grid grid-cols-1 gap-3">
			<button
				class="flex w-full items-center justify-center space-x-2 rounded-md border border-gray-700 bg-gray-800 p-3 text-sm font-medium text-gray-200 shadow-sm transition-colors duration-200 hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-500"
			>
				<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
					<path
						d="M12.0001 4.75C12.0001 4.542 11.9831 4.338 11.9541 4.135H12.0001C15.8271 4.135 19.1411 6.845 20.3561 10.457C20.7391 11.603 20.9321 12.802 20.9321 14.001C20.9321 19.387 17.2511 23.365 12.0001 23.365C6.74906 23.365 3.06806 19.387 3.06806 14.001C3.06806 12.802 3.26106 11.603 3.64406 10.457C4.85906 6.845 8.17306 4.135 12.0001 4.135H12.0001V4.75ZM12.0001 5.365C8.94206 5.365 6.27506 7.234 5.26306 10.052C5.06406 10.613 4.93506 11.206 4.88706 11.821H12.0001V5.365ZM12.0001 11.821H19.1131C19.0651 11.206 18.9361 10.613 18.7371 10.052C17.7251 7.234 15.0581 5.365 12.0001 5.365V11.821ZM12.0001 22.135C15.9321 22.135 19.1131 19.231 19.1131 14.001C19.1131 13.068 18.9891 12.164 18.7561 11.306H12.0001V22.135ZM12.0001 11.306H4.88706C4.65406 12.164 4.53006 13.068 4.53006 14.001C4.53006 19.231 7.71106 22.135 12.0001 22.135V11.306ZM12.0001 4.135H12.0001V4.75V4.135Z"
					/>
				</svg>
				<span>Google</span>
			</button>
			<button
				class="flex w-full items-center justify-center space-x-2 rounded-md border border-gray-700 bg-gray-800 p-3 text-sm font-medium text-gray-200 shadow-sm transition-colors duration-200 hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-gray-500"
			>
				<svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
					<path
						d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.046.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.615.801.576 4.765-1.589 8.192-6.089 8.192-11.385 0-6.627-5.373-12-12-12z"
					/>
				</svg>
				<span>GitHub</span>
			</button>
		</div>
	</div>
</div>
