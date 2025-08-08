<script>
	import Card from '$lib/components/card.svelte'
	import Progress from '$lib/components/progress.svelte'
</script>

<main>
	<h1
		class="text-preset-1 mx-auto max-w-xl text-center text-balance text-neutral-900 dark:text-neutral-100"
	>
		Analyze your text in real-time.
	</h1>

	<section>
		<textarea
			name="text"
			id="text"
			placeholder="Start typing here… (or paste your text)"
			class="text-preset-3 mt-12 mb-3 min-h-52 w-full resize-none rounded-xl bg-neutral-100 p-5 text-neutral-700 outline-0 focus:outline-2 focus:outline-purple-500 dark:bg-neutral-800 dark:text-neutral-200"
		></textarea>

		<div class="flex items-center justify-between">
			<div class="flex gap-6">
				<label for="exclude-spaces" class="label">
					<input type="checkbox" name="exclude-spaces" id="exclude-spaces" class="size-4" />
					<span class="select-none">Exclude Spaces</span>
				</label>

				<label for="limit" class="label">
					<input type="checkbox" name="limit" id="limit" class="size-4" />
					<span class="select-none">Set Character Limit</span>
				</label>
			</div>

			<p>Approx. reading time: 1 minute</p>
		</div>
	</section>

	<section class="mt-12 mb-6 grid grid-cols-3 gap-4">
		<Card count={0} name="Total Characters" class="bg-purple-400" icon="shape-01.svg" />
		<Card count={0} name="Word Count" class="bg-yellow-500" icon="shape-02.svg" />
		<Card count={0} name="Sentence Count" class="bg-orange-500" icon="shape-03.svg" />
	</section>

	<section>
		<h3 class="text-preset-2">Letter Density</h3>

		<div class="mt-5 space-y-3">
			<Progress letter="E" progressValue={0.25} count={0} />
			<Progress letter="Z" progressValue={0.1} count={0} />
		</div>
	</section>
</main>
