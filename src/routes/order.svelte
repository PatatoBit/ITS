<script lang="ts">
	import { PrismaClient } from '@prisma/client'
	const prisma = new PrismaClient()
</script>

<div class="fullflex">
	<div class="w-1/2">
		<input class="w-full text-3xl text-center shadow-md m-2" type="text" placeholder="Title">
		<textarea class="text-lg w-full rounded-md p-2 shadow-lg" cols="30" rows="10" placeholder="Optional Description"></textarea>
	</div>
	<button class="foodsubmit font-bold">Submit</button>
</div>