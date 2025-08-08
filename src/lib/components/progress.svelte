<script lang="ts">
	import { Tween } from 'svelte/motion'
	import { cubicOut } from 'svelte/easing'

	type Props = {
		letter: string
		progressValue: number
		count: number
	}

	const { letter, progressValue, count }: Props = $props()

	const progress = new Tween(progressValue, {
		duration: 400,
		easing: cubicOut
	})
</script>

<article class="flex items-center gap-3.5">
	<span>{letter}</span>
	<progress value={progress.current}></progress>
	<span>{count} (15.4%)</span>
</article>
