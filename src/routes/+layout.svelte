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
	<meta property="og:title" content="FakeGame" />
	<meta
		property="og:description"
		content="Dominion 3:03:00 am 31/07/23 Monday in 13 hours ⌛1:00 👥 0/2"
	/>
	<meta
		property="og:image"
		content="https://firebasestorage.googleapis.com/v0/b/undeadontime.appspot.com/o/gamesImages%2F15263e0e-45b3-4d26-b8ee-6d6cfbc588c5.png?alt=media&token=745cbeec-2dcc-4719-b7cf-0a987363dff0"
	/>
	<meta property="og:url" content="Your URL Here" />
	<meta property="og:site_name" content="Your Site Name Here" />
	<meta property="og:type" content="website" />
</svelte:head>

<Heading />
<slot />
<Footer />
