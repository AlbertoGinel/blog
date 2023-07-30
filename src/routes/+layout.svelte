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

<!-- svelte-ignore a11y-img-redundant-alt -->
<svelte:head>
	<meta property="og:title" content="Your Title Here" />
	<meta property="og:description" content="Your Description Here" />
	<meta
		property="og:image"
		content="https://cdnb.artstation.com/p/assets/images/images/056/598/487/large/blanca-maeso-793c6688-f8b1-4a65-9d57-c6294bc08a1f.jpg?1669657042"
	/>
	<meta property="og:url" content="Your URL Here" />
	<meta property="og:site_name" content="Your Site Name Here" />
	<meta property="og:type" content="website" />
</svelte:head>

<Heading />
<slot />
<Footer />
