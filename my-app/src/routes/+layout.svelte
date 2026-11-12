<script lang="ts">
	import favicon from '#lib/assets/favicon.svg';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<button><a href='/'>home</a></button>
	<button><a href='/name'>name</a></button>
	<button><a href='/cat'>cat</a></button>
</svelte:head>

{@render children()}
