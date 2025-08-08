<script lang="ts">
	import type { SvelteHTMLElements } from 'svelte/elements'
	type Props = SvelteHTMLElements['article'] & {
		count: number
		name: string
		icon: string
	}

	let { count, name, icon, class: CLASS, ...rest }: Props = $props()
</script>

<article
	{...rest}
	class="{CLASS} relative min-w-72 overflow-hidden rounded-xl px-4 py-6 text-black *:relative *:z-10"
	style="background-image: url(/src/lib/assets/{icon});"
>
	<span class="text-preset-1 block">{count}</span>
	<p class="text-preset-3 mt-2">
		{name}
	</p>
</article>

<style>
	article {
		background-repeat: no-repeat;
		background-position: top right -25px;
	}
</style>
