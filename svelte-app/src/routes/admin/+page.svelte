<script>
	let counter = 0;
</script>

<div>ADMIN PANEL.</div>
<div>
	Counter: {counter}
</div>
<button class="btn" on:click={() => counter++}> Increment </button>
<button class="btn" on:click={() => counter--}> Decrement </button>

<style lang="postcss">
</style>
