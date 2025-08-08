<script lang="ts">
	import '../app.css'
	import favicon from '$lib/assets/favicon.svg'
	import Header from '$lib/components/header.svelte'
	let { children } = $props()
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preload" as="font" type="font/woff2" href="/fonts/dm-sans-latin-400-normal.woff2" />
	<link rel="preload" as="font" type="font/woff2" href="/fonts/dm-sans-latin-600-normal.woff2" />
	<link rel="preload" as="font" type="font/woff2" href="/fonts/dm-sans-latin-700-normal.woff2" />
	<script>
		const theme = localStorage.getItem('theme')
		document.documentElement.classList.add(
			!theme || theme === 'system'
				? window.matchMedia('(prefers-color-scheme: dark)').matches
					? 'dark'
					: 'light'
				: theme
		)
	</script>
</svelte:head>

<div class="mx-auto w-full max-w-[990px] pt-8 pb-16">
	<Header />
	{@render children?.()}
</div>
