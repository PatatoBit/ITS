<script lang="ts">
	import Nav from '$lib/components/Nav.svelte'
	import Signin from '$lib/components/Signin.svelte';

	let loggedIn:boolean = false;
</script>

<div class="fullflex">
	<h1 class="select-none text-6xl sm:text-9xl mb-6 font-extrabold">ITS</h1>
	{#if loggedIn}
		<Nav />
	{:else}
		 <Signin />
	{/if}
</div>
