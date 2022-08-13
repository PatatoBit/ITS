<script lang="ts">
	import { auth } from '../firebase';

	import Nav from '$lib/components/Nav.svelte'
	import Signin from '$lib/components/Signin.svelte';


	let loggedIn:boolean = false;
	let username: string | null;

	auth.onAuthStateChanged(user => {
		if (user){
			loggedIn = true;
			username = user.displayName;
		}
		else loggedIn = false;
	})



</script>

<div class="fullflex">
	<h1 class="select-none text-6xl sm:text-9xl mb-6 font-extrabold">ITS</h1>
	{#if loggedIn}
		<Nav username={username}/>
	{:else}
		 <Signin />
	{/if}
</div>
