<script>
	import { theme } from '$lib/stores/theme'
	import Logo from '../assets/logo.svg'
	import Sun from '../assets/sun.svg'
	import Moon from '$lib/assets/moon.svg'
</script>

<header>
	<div class="flex items-center justify-between py-4">
		<div class="flex items-center gap-3">
			<img src={Logo} alt="Charater counter logo" />
			<h2 class="text-preset-2">Character Counter</h2>
		</div>

		<button
			onclick={() => theme.toggle()}
			class="grid size-11 cursor-pointer place-content-center rounded-lg bg-neutral-100 transition-all duration-500 dark:bg-neutral-700"
		>
			{#if $theme === 'dark'}
				<img src={Sun} alt="Sun logo" />
			{:else}
				<img src={Moon} alt="Sun logo" />
			{/if}
		</button>
	</div>
</header>
