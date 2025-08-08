<script lang="ts">
	import '../app.css'
	import favicon from '$lib/assets/favicon.svg'
	import Header from '$lib/components/header.svelte'

	let { children } = $props()
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<div class="mx-auto w-full max-w-[990px] pt-8 pb-16">
	<Header />
	{@render children?.()}
</div>
