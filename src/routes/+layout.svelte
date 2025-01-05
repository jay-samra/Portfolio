<svelte:head>
  <title>Jagroop Singh's Portfolio</title>
  <meta name="description" content="jagroop singh's personal portfolio website, 2025">
  <meta name="keywords" content="calfornia state university sacramento, jagroop singh, computer science">
  <meta name="author" content="jagroop singh">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</svelte:head>

<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css';
	// import 'tailwindcss/t'
	import '@fontsource/space-grotesk/500.css';
	let { children } = $props();

</script>

<ParaglideJS {i18n}>
	{@render children()}
</ParaglideJS>



