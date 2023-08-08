<script>
	import '@skeletonlabs/skeleton/themes/theme-rocket.css';
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	import '../app.postcss';

	import { computePosition, autoUpdate, offset, shift, flip, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';

	import { autoModeWatcher } from '@skeletonlabs/skeleton';
	import Navbar from '$lib/components/Navbar.svelte';

	storePopup.set({ computePosition, autoUpdate, offset, shift, flip, arrow });
</script>

<svelte:head>{@html `<script>${autoModeWatcher.toString()} autoModeWatcher();</script>`}</svelte:head>
<Navbar links={[
	{ name: 'Home', href: '/home' },
	{ name: 'Admin', href: '/admin' },
]}>

</Navbar>
<!-- Page Route Content -->
<slot />

<style lang="postcss">

</style>