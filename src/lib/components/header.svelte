<script>
	import Logo from '../assets/logo.svg'
	import Sun from '../assets/sun.svg'
</script>

<header>
	<div class="flex items-center justify-between py-4">
		<div class="flex items-center gap-3">
			<img src={Logo} alt="Charater counter logo" />
			<h2 class="text-preset-2">Character Counter</h2>
		</div>

		<div
			class="grid size-11 cursor-pointer place-content-center rounded-lg bg-neutral-700 transition-colors hover:bg-neutral-600"
		>
			<img src={Sun} alt="Sun logo" />
		</div>
	</div>
</header>
