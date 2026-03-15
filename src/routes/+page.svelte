<script lang="ts">
	import GopayLogo from '$lib/assets/Gopay-Logo.png';
	import { ArrowUpRight } from '@lucide/svelte';
	import CoinBase from '$lib/assets/logo/coinbase.png';
	import Klarna from '$lib/assets/logo/klarna.png';
	import InstaCard from '$lib/assets/logo/instacart.png';
	import card from '$lib/assets/logo/card.png';
	interface ImageItems {
		src: string;
		alt: string;
	}

	interface Currency {
		money: number;
		symbol: string;
	}

	const Currency = [
		{
			money: 100,
			symbol: '$'
		}
	];

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

<nav class="flex h-20 items-center justify-center">
	<span class="w-40"> <img src={GopayLogo} alt="" /></span>
	<div class="flex h-10 items-center justify-between px-10 md:w-4/5">
		<div class="flex items-center gap-12">
			<ul class="hidden gap-4 capitalize md:flex">
				<li><a href="#products">products</a></li>
				<li><a href="#customers">customers</a></li>
				<li><a href="#pricing">pricing</a></li>
				<li><a href="#learn">learn</a></li>
			</ul>
		</div>

		<div class=" hidden gap-4 md:flex">
			<button class="rounded-xl border border-slate-400 bg-white px-5 py-2 capitalize">login</button
			>
			<button
				class="rounded-xl border border-slate-400 bg-blue-500 px-5 py-2 text-blue-50 capitalize"
				>sign up</button
			>
		</div>
	</div>
</nav>

<section class="my-10 flex h-screen md:mx-50">
	<div
		class="m-4 flex h-100 w-full flex-col items-center justify-center gap-10 md:grid md:grid-cols-2"
	>
		<div class=" ">
			<span>
				<h1 class="align-middle text-5xl font-semibold text-slate-800 md:text-7xl md:leading-20">
					<span class="font-bold capitalize">get paid early</span> save automatically all your pay.
				</h1>
				<p class="text-md my-5 text-slate-500 md:text-2xl md:leading-10">
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
					class="rounded-lg p-2 outline-none md:w-80"
					placeholder="your business email"
				/>
				<button
					class=" md:text-md flex items-center justify-center gap-2 rounded-lg bg-blue-500 px-3 text-sm font-thin text-blue-50 capitalize md:px-6 md:py-3"
					>get started <ArrowUpRight /></button
				>
			</div>

			<div class="flex items-center gap-3 py-4">
				{#each ImageItems as image}
					<img src={image.src} class="h-fit w-20 md:w-30" alt={image.alt} />
				{/each}
			</div>
		</div>
		<div class="">
			<img src={card} alt="" />
			<!--  -->
		</div>
	</div>
</section>
