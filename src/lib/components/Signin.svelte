<script>
	import { auth } from '../../firebase';
	import { signInWithPopup, GoogleAuthProvider } from 'firebase/auth';
	const provider = new GoogleAuthProvider();

	function signIn(){
		signInWithPopup(auth, provider)
		.then((result) => {
			console.log(result);
		})
		.catch((err) => {
			console.log(err);
		});
	}
</script>

<button class="flex text-3xl border-2 rounded-md bg-blue-600 text-white px-4 py-2" on:click={signIn}>Sign in</button>