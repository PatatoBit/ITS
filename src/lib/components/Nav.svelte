<script lang="ts">
	import { auth } from '../../firebase';

	export let username: string | null;

</script>

<div class="navbar">
	<a href="/order">
		<p>Order Food 🍗</p>
	</a>
	<a href="/communiquette">
		<p>Communiquette 📋</p>
	</a>
	<a href="/skedew">
		<p>Skedew 📅</p>
	</a>
</div>

<div class="flex">
	<h1 class="text-2xl px-4 py-2 border-2 border-blue-200 rounded-md">Logged in as {username}</h1>
	<button class="signout" on:click={() => auth.signOut()}>Sign Out</button>
</div>
