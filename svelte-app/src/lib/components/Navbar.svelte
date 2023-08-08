<script>
	import { popup } from '@skeletonlabs/skeleton';
	import NavbarLink from './NavbarLink.svelte';

	export let links;
	const popupCombobox = {
		event: 'focus-click',
		target: 'popupCombobox',
		placement: 'bottom',
		closeQuery: '.listbox-item'
	};
</script>

<div class="sticky top-0 w-full p-2 flex flex-row justify-between bg-primary-100-800-token">
	<a href="/home" class="btn px-3 variant-outline-primary"> Wadi Makkah </a>

	<button class="btn justify-between md:hidden" use:popup={popupCombobox}>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			fill="none"
			viewBox="0 0 24 24"
			stroke-width="1.5"
			stroke="currentColor"
			class="w-6 h-6"
		>
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
			/>
		</svg>
	</button>
	<div class="hidden md:flex flex-row-reverse">
		{#each links as { name, href }}
			<NavbarLink {name} {href} />
		{/each}
	</div>
	<div class="card w-32 shadow-xl p-2" data-popup="popupCombobox">
		<div>
			{#each links as { name, href }}
				<NavbarLink {name} {href} />
			{/each}
		</div>
		<div class="arrow bg-surface-100-800-token" />
	</div>
</div>

<style lang="postcss">
</style>
