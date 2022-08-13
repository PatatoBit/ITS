<script>
	import { auth } from '../../firebase';

	import { signInWithPopup, GoogleAuthProvider } from 'firebase/auth';
	const provider = new GoogleAuthProvider();
	import Google from '$lib/assets/Google.png'

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

<img class="cursor-pointer" src={Google} alt="Google Icon" on:click={signIn}>