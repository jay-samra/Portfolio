<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css';
	// import 'tailwindcss/t'
	let { children } = $props();


	import '@fontsource-variable/cinzel';
</script>

<ParaglideJS {i18n}>
	{@render children()}
</ParaglideJS>

