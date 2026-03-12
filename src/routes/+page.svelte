<script lang="ts">
	import GopayLogo from '$lib/assets/Gopay-Logo.png';
	import { ArrowUpRight } from '@lucide/svelte';
	import CoinBase from '$lib/assets/logo/coinbase.png';
	import Klarna from '$lib/assets/logo/klarna.png';
	import InstaCard from '$lib/assets/logo/instacart.png';

	interface ImageItems {
		src: string;
		alt: string;
	}

	const ImageItems = [
		{
			src: CoinBase,
			alt: 'coinbase'
		},
		{
			src: Klarna,
			alt: 'klarna'
		},
		{
			src: InstaCard,
			alt: 'instacard'
		}
	];
</script>

<nav class="flex justify-center">
	<div class="flex h-17 w-4/5 items-center justify-between px-10">
		<div class="flex items-center gap-12">
			<span class="w-40"> <img src={GopayLogo} alt="" /></span>
			<ul class="flex gap-4 capitalize">
				<li><a href="#products">products</a></li>
				<li><a href="#customers">customers</a></li>
				<li><a href="#pricing">pricing</a></li>
				<li><a href="#learn">learn</a></li>
			</ul>
		</div>

		<div class=" flex gap-4">
			<button class="rounded-xl border border-slate-400 bg-white px-5 py-2 capitalize">login</button
			>
			<button
				class="rounded-xl border border-slate-400 bg-blue-500 px-5 py-2 text-blue-50 capitalize"
				>sign up</button
			>
		</div>
	</div>
</nav>

<section class="my-10 flex md:mx-50">
	<div class="m-4 grid h-100 w-full grid-cols-2">
		<div class=" ">
			<span>
				<h1 class="align-middle text-7xl leading-20 font-semibold text-slate-800">
					<span class="font-bold capitalize">get paid early</span> save automatically all your pay.
				</h1>
				<p class="my-5 text-2xl leading-10 text-slate-500">
					support small bussines with simple invoicing, powerful integrations, and cash flow
					management tools.
				</p>
			</span>
			<div class=" flex w-fit rounded-xl border border-slate-400 p-1 pl-2">
				<!-- business name -->
				<input
					type="text"
					name=""
					id=""
					class="w-80 rounded-lg p-2 outline-none"
					placeholder="your business email"
				/>
				<button
					class=" flex items-center justify-center gap-2 rounded-lg bg-blue-500 px-6 py-3 font-thin text-blue-50 capitalize"
					>get started <ArrowUpRight /></button
				>
			</div>

			<div class="flex items-center gap-3 py-4">
				{#each ImageItems as image}
					<img src={image.src} class="h-fit w-30" alt={image.alt} />
				{/each}
			</div>
		</div>
		<div class="bg-blue-700">
			<img src="" alt="" />
		</div>
	</div>
</section>
