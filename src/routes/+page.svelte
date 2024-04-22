<script>
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';

	onMount(() => {
		gsap.from('.first', { opacity: 0, y: 50, duration: 0.5 });
		gsap.from('.second', { opacity: 0, y: 50, duration: 0.5, delay: 0.5 });
		gsap.from('.third', { opacity: 0, y: 50, duration: 0.5, delay: 1.0 });
		gsap.from('.fourth', { opacity: 0, x: 50, duration: 0.5, delay: 1.5 });
	});

	function scaleUp() {
		gsap.to('.third', { scale: 1.1, duration: 0.3 });
	}

	function scaleDown() {
		gsap.to('.third', { scale: 1, duration: 0.3 });
	}
</script>

<img
	src="/gradient.png"
	alt="Gradient"
	class="absolute hidden w-1/2 lg:block -z-10 right-12 fourth"
/>
<section class="flex h-screen pt-56 lg:px-32">
	<div class="w-1/2">
		<h1 class="mb-8 text-6xl font-bold leading-relaxed first">
			Learn Arabic Easily with Our Interactive Platform.
		</h1>
		<h2 class="mb-4 text-3xl font-medium leading-relaxed second">
			All you need to learn Arabic is here!
		</h2>
		<button
			on:mouseenter={scaleUp}
			on:mouseleave={scaleDown}
			class="px-4 py-2 text-lg font-medium rounded-xl third bg-primary">Subscribe now</button
		>
	</div>
</section>
<section class="lg:mx-32 lg:py-32">
	<h2 class="text-4xl font-bold text-center lg:mb-4">Benefits and Features</h2>
	<h3 class="font-semibold text-center lg:text-2xl">
		We provide a structured plan so you can start learning directly.
	</h3>
	<div class="flex flex-row justify-center gap-32 mt-16">
		<div>
			<img src="/standing-learning.png" alt="A man working on his laptop on his standing desk" />
		</div>
		<div class="flex flex-col justify-center gap-6">
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>1</span>
				</div>
				<div>Learn at your own pace</div>
			</div>
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>2</span>
				</div>
				<div>A platform that contains everything to learn Arabic</div>
			</div>
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>3</span>
				</div>
				<div>Affordable subscription</div>
			</div>
		</div>
	</div>
</section>

<section class="lg:mx-32 lg:py-32">
	<h2 class="text-4xl font-bold text-center lg:mb-4">Testimonials</h2>
	<h3 class="font-semibold text-center lg:text-2xl">
		See what fellow students say about our platform.
	</h3>
	<div class="flex flex-col items-center justify-center w-full gap-8 py-8 mt-16">
		<h1 class="w-4/5 text-4xl leading-relaxed secondary-content">
			<span class="text-5xl font-bold">"</span>Lorem Ipsum is simply dummy text of the printing and
			typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the
			1500s<span class="text-5xl font-bold">"</span>
		</h1>
		<div class="flex items-center gap-4">
			<div class="w-12 h-12 overflow-hidden bg-black rounded-full">
				<img src="https://rairaksa.github.io/assets/img/rai.jpg" />
			</div>
			<div class="flex flex-col tracking-wider">
				<label class="text-base font-bold text-gray-600">Rai Raksa Muhamad</label>
				<label class="text-sm font-normal text-gray-400">Student since May 2023</label>
			</div>
		</div>
	</div>
</section>

<section class="lg:mx-32 lg:py-32">
	<h2 class="text-4xl font-bold text-center lg:mb-4">Here is how it works</h2>
	<h3 class="font-semibold text-center lg:text-2xl">
		There are 3 main aspects to learning a language: Grammar, Vocabulary, and Speaking. We provide
		all of them.
	</h3>
	<div class="flex flex-row justify-center gap-32 mt-16">
		<div>
			<img src="/standing-learning.png" alt="A man working on his laptop on his standing desk" />
		</div>
		<div class="flex flex-col justify-center gap-6">
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>1</span>
				</div>
				<div>Learn at your own pace</div>
			</div>
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>2</span>
				</div>
				<div>A platform that contains everything to learn Arabic</div>
			</div>
			<div class="flex flex-row items-center gap-4 text-xl font-medium">
				<div
					class="flex items-center justify-center w-12 h-12 border-2 rounded-full border-accent lg:text-xl"
				>
					<span>3</span>
				</div>
				<div>Affordable subscription</div>
			</div>
		</div>
	</div>
</section>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>
