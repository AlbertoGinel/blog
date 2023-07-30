<script lang="ts">
	import { page } from '$app/stores'
	import { handleSession } from '@lucia-auth/sveltekit/client'
	import Heading from './heading.svelte'
	import Footer from './footer.svelte'

	import '@skeletonlabs/skeleton/themes/theme-crimson.css'
	import '@skeletonlabs/skeleton/styles/all.css'
	import '../app.postcss'

	handleSession(page)
</script>

<svelte:head>
	<title>Game Board</title>
	<link rel="icon" href="https://fav.farm/🔥" />
	<img
		src="https://cdnb.artstation.com/p/assets/images/images/056/598/487/large/blanca-maeso-793c6688-f8b1-4a65-9d57-c6294bc08a1f.jpg?1669657042"
		alt="Your image description"
	/>
</svelte:head>

<Heading />
<slot />
<Footer />
