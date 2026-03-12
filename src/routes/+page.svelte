<script lang="ts">
	import GopayLogo from '$lib/assets/Gopay-Logo.png';
</script>

<nav class="flex justify-center bg-gray-100">
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
			<button class="rounded-xl border border-slate-400 bg-white px-5 py-2 capitalize">login</button>
			<button class="rounded-xl border border-slate-400 bg-blue-500 text-blue-50 px-5 py-2 capitalize"
				>sign up</button
			>
		</div>
	</div>
</nav>


